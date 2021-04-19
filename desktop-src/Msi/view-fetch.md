---
description: 如果結果集中有多個資料列，則 View 物件的 Fetch 方法會抓取資料行資料的下一個資料列，否則會是 Null。 呼叫 Fetch 方法之前的 Execute 方法。
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. Fetch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992793"
---
# <a name="viewfetch-method"></a>View. Fetch 方法

如果結果集中有多個資料列，則 [**View**](view-object.md)物件的 Fetch 方法會 **抓取** 資料行資料的下一個資料列，否則會是 Null。 呼叫 **Fetch** 方法之前的 [**Execute**](view-execute.md)方法。

## <a name="syntax"></a>語法


```JScript
View.Fetch()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

您應該使用相同的 [**記錄**](record-object.md) 物件來取出多個資料列中的資料，否則物件應移出範圍以外的方式釋出。 您可以使用「如果 FetchRecord 為 Nothing」語法來測試結果集結尾的記錄。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




