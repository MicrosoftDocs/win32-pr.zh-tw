---
description: CGenericList 類別範本，它會執行特定類型的清單。 如需詳細資訊，請參閱 CBaseList。
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: 'CGenericList 類別 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994766"
---
# <a name="cgenericlist-class"></a>CGenericList 類別

![cgenericlist 類別階層](images/list01.png)

執行 `CGenericList` 類型特定清單的類別樣板。 如需詳細資訊，請參閱 [**CBaseList**](cbaselist.md)。

若要使用這個範本，請使用樣板 `CGenericList` 引數（定義清單中的物件類型）宣告類型的變數。 例如，下列語句會宣告 [**CBaseFilter**](cbasefilter.md) 物件的清單：


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



為了方便起見，Wxlist 會定義下列清單類型：

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| 公用方法                                          | Description                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**CGenericList**](cgenericlist-cgenericlist.md)       | 函式方法。                                                      |
| [**~ CGenericList**](cgenericlist--cgenericlist.md)     | 函式方法。                                                       |
| [**GetHeadPosition**](cgenericlist-getheadposition.md) | 抓取清單中第一個專案的位置。                    |
| [**GetTailPosition**](cgenericlist-gettailposition.md) | 抓取清單最後一個專案的位置。                     |
| [**GetCount**](cgenericlist-getcount.md)               | 捕獲清單中的專案數。                               |
| [**GetNext**](cgenericlist-getnext.md)                 | 抓取指定位置的專案，並將位置往前移。 |
| [**Get**](cgenericlist-get.md)                         | 在指定位置抓取專案。                            |
| [**GetHead**](cgenericlist-gethead.md)                 | 抓取清單開頭的專案。                              |
| [**RemoveHead**](cgenericlist-removehead.md)           | 移除清單中的第一個專案。                                      |
| [**RemoveTail**](cgenericlist-removetail.md)           | 移除清單中的最後一個專案。                                       |
| [**移除**](cgenericlist-remove.md)                   | 移除位於指定位置的專案。                              |
| [**AddBefore**](cgenericlist-addbefore.md)             | 將專案或清單插入指定的位置之前。                   |
| [**AddAfter**](cgenericlist-addafter.md)               | 將專案或清單插入指定的位置之後。                    |
| [**AddHead**](cgenericlist-addhead.md)                 | 將專案或清單加入至清單的前方。                           |
| [**AddTail**](cgenericlist-addtail.md)                 | 將專案或清單附加至清單結尾。                          |
| [**Find**](cgenericlist-find.md)                       | 抓取保留指定專案的第一個位置。              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




