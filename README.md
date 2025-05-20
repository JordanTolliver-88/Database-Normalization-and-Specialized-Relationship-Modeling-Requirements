# Database-Normalization-and-Specialized-Relationship-Modeling-Requirements

**Modeling Historical**
- For use in analyzing providers (doctors) and their effectiveness – if a patient changes primary care doctors we would like to be able to keep track of these changes. This will also aid in patient care tracking throughout their life. We would like to be able to keep a record of each patient’s charts and which doctors may have provided information on them.

![historical](https://github.com/user-attachments/assets/bc4e5498-2f09-46dd-9bd4-cc3db274cf72)

**3 stages of normalization**

1.	1st normal form states that all attributes have a single value - no multivalued attributes. For example : each patient can only have one primary doctor, each doctor can only have one specialty etc.
2.	2nd normal form says that all attributes must be dependent on the entire key of the entity. For example we need to know each drug’s name, purpose and side effects but if we include this in the Prescription entity it will be dependent only on what drug is prescribed not who it’s for or what doctor prescribed it – so it does not belong in the same entity as the prescription information itself.
3.	3rd normal form states that no non-UID attribute can be dependent on another non- UID attribute. For example : A patient’s insurance ID number will determine what insurance company they are insured with. The ID number determines the insurance company’s name.

![Picture1](https://github.com/user-attachments/assets/10e4a652-d41a-4f6f-9140-c5d5e1e37229)

**Arcs**

- Each prescription issued by a doctor must be refillable or non-refillable. It can’t be both.
![arcs](https://github.com/user-attachments/assets/728872f8-f50d-48ab-8237-f2b84f16aff5)

**Recursive Relationships**

Some patients in the patient entity may be part of the same family and be covered by the same insurance – we would like to designate a field in the patient entity showing who is the insurance holder for each patient – this field would be the patient ID number of the person holding the insurance for the family.![image](https://github.com/user-attachments/assets/beebe565-07fa-40c1-a214-f926fdd53f7d)

![recursive](https://github.com/user-attachments/assets/fc05653a-5149-40fc-96a4-a17e056272c6)
