# StoneWareP6
OpenClassrooms Project 6 : Design and creation of a database with stored procedure
 

## Entity-relationship diagram
See the database design :


## Example - set the assignments data source
 
    EXEC spProductVersionDateRangeSearchOutstanding
		@ProductId = 1,
		@VersionId = 1,
		@KeyWords = 'admin granting',
		@StartDate = '2022-10-10',
		@EndDate = '2022-10-20'

![StonewareERD](https://github.com/PinsonMarc/StoneWareP6/blob/relational-database-basics/ERD.png)

the .bacpac also include a 50+ issues dataset
