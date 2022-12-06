# Quantum Programming Templates 

Quantum Programming Demonstration Exercises (Demo Templates)
These are the basic examples that are provided with qisket's notebook for instance. Also programming quantum computers will be a  very useful resource as well. 

We will be demonstrating with  IBM's language qisket. There are many others that we can use  including tket,  ___ , ___ , and more. 

First step before moving onto the exercises  (for  qisket examples):  
```
import qiskit

# Qiskit quantum circuits libraries

quantum_circuit = qiskit.circuit.library.QuantumVolume(5)

quantum_circuit.measure_all()

quantum_circuit.draw()

# prepare your circuit to run

from qiskit import IBMQ

# Get the API token in

# https://quantum-computing.ibm.com/

IBMQ.save_account("YOUR TOKEN")

provider = IBMQ.load_account()

backend = provider.get_backend('ibmq_quito')

optimized_circuit = qiskit.transpile(quantum_circuit, backend)

optimized_circuit.draw()

# run in real hardware

job = backend.run(optimized_circuit)

retrieved_job = backend.retrieve_job(job.job_id())

result = retrieved_job.result()

print(result.get_counts())
```
  
1.  Exercise 1 - Description
    
2.  Exercise 2 - Description
    
3.  Exercise 3 - Description
    
4.  Exercise 4 - Description
    
5.  Exercise 5 - Description
    
6.  Add to appendices
    


Further resources --> qisket notebook,  programming with  quantum computers textbook by Eric Johnston

References: 
- https://lab.quantum-computing.ibm.com/hub/spawn-pending/5d798394a5375400195c9658?next=%2Fhub%2Fuser%2F5d798394a5375400195c9658%2Flab%2Ftree%2Fqiskit-textbook%2Fgetting-started%2Fexample.ipynb
- 