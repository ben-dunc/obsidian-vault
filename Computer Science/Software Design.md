
--- 
# UML Class Diagrams
- Modeling is a well accepted method of creating a system.
- There were lots of peeps who were making lots of different approaches - kind of annoying that there were so many different models.
- They got a bunch of popular model authors and they came up with UML.

# UML: Unified Modeling Language
- Structural
	- Class diagram
	- Package diagram
- Behavioral
	- Sequence Diagram
*There are more diagrams but we are not learning them in this class...*

### Three ways to use UML
1. Blueprint
	- Matches the "Big Design Up Front" paradigm
	- Not used anymore because code and the design change as time goes. Once it changes, the "Big Design" is useless.
2. Programming Language
	- Used in code generation tools (popular in the 90s -- havn't seen this much lately)
3. Sketch
	- Matches the Agile software development paradigm

## Class Diagrams at the conceptual level
- Classes are represented by a box, typically with a common name
- You can divide it into three parts (boxes): the name, attributes, and method sections.
	- A high-level diagram is just the name
	- A **conceptual diagram** is the first two boxes
- A diagram doesn't contain every detail.
- '+' means public, '-' means private, '#' means private, '/' derived, '\_' static, '~' static
- If a name is underlined, that means that it is a *instance* of an object, not a class definition.
	- Not always used, I _think_

### Associations
- Associations are represented by lines
- There's a cardinality of associations
	- '\*' represents many
	- but it represents the number of associations between things
	- 1 : only one
	- 0..1 : 0 to 1 (or another number)
	- * : (many)
	- 1..* : 1 (or another number) to many
	- n..m : (many - maybe one number, n, to another number, m)
- The floating arrow next to the association line is the least-important thing - it's the _reading direction indicator_, telling us which direction to read the association.
- __Association term__
- **Roles**: Add roles to association, goes next to end of association line
- **Association Arrow**: With the example where person is associated with and pointing to Address, the solid arrow means that we can access an address via a Person, but, given an Address we can't determine the Person associated with it.
	- You can also show the association by having an instance of the class in the attributes section of a class box.
	- Note that the inherited or subtyped class doesn't know who it's children are but the children do know from whom they're inheriting, thus the arrow points to the inherited class.
- **Aggregation**: represented by a hollow diamond at the end of an association line
	- In this case, the diamond is near _Company_
	- Can be read as Person is subpart of a Company
		- A person is a subpart of a company and can be associated with 0 or more companies (can exist without a company). A company 
	- Some poeple prefer to just use associations - you can use both
	- Can use "comb" representation
- **Composition**: represented by a solid diamond at the end of an association line
	- In this case, the diamond is near _Car_, from _Car Part_
	- Can be read as _Car Part_ cannot exist unless it is part of a car.
		- A car has 1 or more car parts but a car part has only one car with which it cannot exist.
	- Notice that there is no association constraint next to the black diamond because it is always 1.
- **General Contraints/Notes**: A note (looks like a sticky note - a box with a bent corner) and is connected to the class with a *dashed* line.
- **Dependency**: A dashed line with a arrow at the end.
	- Person - - - - - - - - > Address
	- Person is dependent on Address.
	- This means that code is dependent on other.
- **Association Class**: Usefule when thinking of an association as an object (for instance - marraige information between Husband and Wife objects)
- **N-ary Associations** complicated and we are probs not going to use it much