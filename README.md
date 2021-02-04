<h1 align="center">ReCap Project : Araba Kiralama Sistemi</h1> 


## Introduction
- **Entities, DataAccess, Business ve Console katmanlarından oluşan araba kiralama console projesidir. Şimdilik Car, Brand ve Color nesnelerinden ve onun operasyonlarından oluşan bu küçük proje zamanla geliştirilecektir.**
- **Bir önceki projemde N-Katmanlı Mimari yapısını kullanmıştım ve [README.md](https://github.com/gulceselim/ReCapDemo/blob/master/README.md) dosyasında elimden geldiğince açıklamaya çalışmıştım isterseniz bakabilirsiniz.**

## Changes
- Artık projemiz bir memory üzerinde değil, database üzerinde çalışıyor ✔
- EntityFramework dosyaları eklendi ✔

## Layers
### Entities Layer
#### Concrete Classes
1. [Car.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Entities/Concrete/Car.cs)
2. [Brand.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Entities/Concrete/Brand.cs)
3. [Color.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Entities/Concrete/Color.cs)

#### Abstract Classes
1. [IEntity.cs](https://github.com/gulceselim/re-cap-project-with-csharp/tree/main/Entities/Abstract)

### Business Layer
#### Concrete Classes
1. [CarManager.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Business/Concrete/CarManager.cs)
2. [BrandManager.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Business/Concrete/BrandManager.cs)
3. [ColorManager.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Business/Concrete/ColorManager.cs)
  
#### Abstract Classes
1. [ICarService.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Business/Abstract/ICarService.cs)
2. [IBrandService.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Business/Abstract/IBrandService.cs)
3. [IColorService.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/Business/Abstract/IColorService.cs)

### DataAccess Layer
#### EntityFramework
1. [Repository/EfCarDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Concrete/EntityFramework/Repository/EfCarDal.cs)
2. [Repository/EfBrandDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Concrete/EntityFramework/Repository/EfBrandDal.cs)
3. [Repository/EfColorDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Concrete/EntityFramework/Repository/EfColorDal.cs)
4. [Context/RentACarContext.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Concrete/EntityFramework/Context/RentACarContext.cs)

#### InMemory
1. [InMemory/InMemoryCarDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Concrete/InMemory/InMemoryCarDal.cs)
2. [InMemory/InMemoryBrandDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Concrete/InMemory/InMemoryBrandDal.cs)
3. [InMemory/InMemoryColorDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Concrete/InMemory/InMemoryColorDal.cs)


#### Abstract Classes
1. [ICarDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Abstract/ICarDal.cs)
2. [IBrandDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Abstract/IBrandDal.cs)
3. [IColorDal.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Abstract/IColorDal.cs)
4. [IEntityRepository.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/DataAccess/Abstract/IEntityRepository.cs)

### UI Layer (Console)
1. [Program.cs](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/ConsoleUI/Program.cs)

### SQL Query
1. [RentACarSQLQuery.sql](https://github.com/gulceselim/re-cap-project-with-csharp/blob/main/RentACarSQLQuery.sql)

## Tables
#### Car
Variable Name | Data Type
------------ | -------------
CarId | int
BrandId | int
ColorId | int
ModelYear | string
DailyPrice | decimal
Description | string

#### Color
Variable Name | Data Type
------------ | -------------
ColorId | int
ColorName | string

#### Brand
Variable Name | Data Type
------------ | -------------
BrandId | int
BrandName | string

## Output
![Console Output](https://user-images.githubusercontent.com/43720773/106918708-7f733780-671a-11eb-8f5d-cd6880549af4.jpg)

## Files
![Files](https://user-images.githubusercontent.com/43720773/106918756-8bf79000-671a-11eb-9b60-4e20d46ed1d8.jpg)
