---
description: SummaryInfo 物件的保存方法會格式化，並將先前儲存的屬性寫入標準 SummaryInformation 資料流程。
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. 保存方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993386"
---
# <a name="summaryinfopersist-method"></a>SummaryInfo. 保存方法

[**SummaryInfo**](summaryinfo-object.md)物件的 **保存** 方法會格式化，並將先前儲存的屬性寫入標準 SummaryInformation 資料流程。 如果無法成功寫入資料流程，它就會產生錯誤。 只有在設定所有屬性值之後，才會呼叫這個方法一次。 寫入資料流程之後，仍然可以讀取屬性。

## <a name="syntax"></a>語法


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo 定義為 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




