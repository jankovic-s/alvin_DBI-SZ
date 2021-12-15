# NoSQL Modell für alvin Webapp

```plantuml
@startuml

class User {
    *Id : Guid
    *Firstname : string
    *Lastname : string
    *Male : int
    *Birthdate : int
    *Password : string
    *User Type : usertype
    *Costs : List<Cost>
}


class UserType {
    *Id : Guid
    *Name : string
}


class Image  {
    *Persons : List<ImagePerson>
}

class Cost {
    *Id : Guid
    *Name : string
    *IsMonthly : bool
    *Fee : int
}

class Screenshot {
    *Id : Guid
    *User : User
    *Bank : string
}

class Admin {
    *Username : string
}


User *--> UserType
User *--> Cost



@enduml


```