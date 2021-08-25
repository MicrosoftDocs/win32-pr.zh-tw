---
description: 記錄物件的 DataSize 屬性是唯讀屬性，會傳回指定欄位的資料大小。
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 067fc09e65d644413e75ccd8a9c0173e30df8060dff0f772ae5d12705ab610aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912958"
---
# <a name="recorddatasize-property"></a>Record 屬性

[**記錄**](record-object.md)物件的 **DataSize** 屬性是唯讀屬性，會傳回指定欄位的資料大小。 如果資料是資料流程，則會傳回資料流程長度（以位元組為單位）。 如果資料是字串，則會傳回不含 Null 的字串長度。 如果資料是整數，則會傳回值4， (表示整數) 的大小。 如果資料為 Null，則會傳回0。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>屬性值

記錄中值的必要欄位編號（以1為基礎）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




