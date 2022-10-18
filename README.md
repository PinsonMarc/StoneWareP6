# StoneWareP6
OpenClassrooms Project 6 : Design and creation of a database with stored procedure

## Documentation 

### Stored procedure 

| Resolved           | Outstanding | Product  | Version | DateRange           | Search | 
| :-------------: |:-------------:| :-------------: |:-------------:| :-------------: |:-------------:| 
| Only resolved issue| Only Outstanding issue  | Issue on a specified Product using product id| Issue on a specified Version using version id | Created/Resolved in a specified date range | Full-text earch issues using a list of keywords in a string separated with spaces |

---
#### `spOutstanding` & `spResolved`

```sql
EXEC spResolved;
EXEC spOutstanding;
```
---
#### `spProductOutstanding` & `spProductResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |

```sql
EXEC spProductOutstanding;
	@ProductId = 1	
```
---
#### `spProductVersionOutstanding` & `spProductVersionResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |
| VersionId      | int |

```sql
EXEC spProductVersionOutstanding;
	@ProductId = 1,
	@VersionId = 1
```
---
#### `spProductDateRangeOutstanding` & `spProductDateRangeResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |
| StartDate      | datetime |
| EndDate      | datetime |

```sql
EXEC spProductDateRangeOutstanding;
	@ProductId = 1,
	@StartDate = '2022-10-10',
	@EndDate = '2022-10-20'
```
---
#### `spProductVersionDateRangeOutstanding` & `spProductVersionDateRangeResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |
| StartDate      | datetime |
| EndDate      | datetime |
| VersionId      | int |

```sql
EXEC spProductVersionDateRangeOutstanding;
	@ProductId = 1,
	@VersionId = 1,
	@StartDate = '2022-10-10',
	@EndDate = '2022-10-20'
```
---
#### `spSearchOutstanding` & `spSearchResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| KeyWords      | varchar |

```sql
EXEC spSearchOutstanding;
	@KeyWords = 'clicking window'
```
---
#### `spProductSearchOutstanding` & `spProductSearchResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |
| KeyWords      | varchar |

```sql
EXEC spProductSearchOutstanding;	
	@ProductId = 1,
	@KeyWords = 'clicking window'
```
---
#### `spProductVersionSearchOutstanding` & `spProductDateRangeSearchResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |
| VersionId      | int |
| KeyWords      | varchar |

```sql
EXEC spProductVersionSearchOutstanding;	
	@ProductId = 1,
	@VersionId = 1,
	@KeyWords = 'clicking window'
```
---
#### `spProductDateRangeSearchOutstanding` & `spProductVersionSearchResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |
| StartDate      | datetime |
| EndDate      | datetime |
| KeyWords      | varchar |

```sql
EXEC spProductDateRangeSearchOutstanding;	
	@ProductId = 1,
	@StartDate = '2022-10-10',
	@EndDate = '2022-10-20',
	@KeyWords = 'clicking window'
```
---
#### `spProductVersionDateRangeSearchOutstanding` & `spProductVersionDateRangeSearchResolved`

| Parameter        | Type           |
| :------------- |:-------------|
| ProductId      | int |
| VersionId      | int |
| StartDate      | datetime |
| EndDate      | datetime |
| KeyWords      | varchar |

```sql
EXEC spProductVersionDateRangeSearchOutstanding;	
	@ProductId = 1,
	@VersionId = 1,
	@StartDate = '2022-10-10',
	@EndDate = '2022-10-20',
	@KeyWords = 'clicking window'
```

### Returning table description

#### `Outstanding` procedures :
| Name        | Type           |
| :------------- |:-------------|
| Product      | varchar |
| Version     | varchar      |
| OS | varchar   |
| Description | varchar     |
| CreationDate | DateTime     |


#### `Resolved` procedures :
| Name        | Type           |
| :------------- |:-------------|
| Product      | varchar |
| Version     | varchar      |
| OS | varchar   |
| Description | varchar     |
| CreationDate | DateTime     |
| Resolution | varchar     |
| ResolvedDate | DateTime     |
---

## Entity-relationship diagram

See the database design :

![StonewareERD](https://github.com/PinsonMarc/StoneWareP6/blob/relational-database-basics/ERD.png)

the .bacpac also include a 50+ issues dataset
