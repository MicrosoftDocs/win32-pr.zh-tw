---
description: View 物件的 Close 方法會終止查詢執行，並釋放資料庫資源。
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000829"
---
# <a name="viewclose-method"></a>View. Close 方法

[**View**](view-object.md)物件的 **Close** 方法會終止查詢執行，並釋放資料庫資源。

## <a name="syntax"></a>語法


```JScript
View.Close()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

除非已使用 [**Fetch**](view-fetch.md)方法取得結果集的所有資料列，否則必須在 [**View**](view-object.md)物件上再次呼叫 [**Execute**](view-execute.md)方法之前呼叫這個方法。 當視圖終結時，它會在內部呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




