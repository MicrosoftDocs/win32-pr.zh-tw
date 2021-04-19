---
description: 記錄物件的至 convertfrom-stringdata 屬性是讀寫屬性，可將字串資料傳入或傳出記錄內的指定欄位。 如果已儲存整數或物件，則會傳回其字串值。
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: 至 convertfrom-stringdata 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989835"
---
# <a name="recordstringdata-property"></a>至 convertfrom-stringdata 屬性

[**記錄**](record-object.md)物件的 **至 convertfrom-stringdata** 屬性是讀寫屬性，可將字串資料傳入或傳出記錄內的指定欄位。 如果已儲存整數或物件，則會傳回其字串值。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>屬性值

記錄中值的必要欄位編號（以1為基礎）。

## <a name="remarks"></a>備註

不存在之欄位的傳回值為空字串。 若要將記錄字串欄位設定為 null，請使用空的 variant 或空字串。 嘗試在不存在的欄位中儲存值會導致錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




