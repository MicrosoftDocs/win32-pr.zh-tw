---
description: 安裝程式物件的 SummaryInformation 屬性會傳回 SummaryInfo 物件，此物件可用來檢查、更新和加入屬性至封裝或轉換的摘要資訊資料流程中。
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: SummaryInformation 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f671a5424e1008787443a13f2b72e75cb931da2f0783681c360a1b03ad640aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043618"
---
# <a name="installersummaryinformation-property"></a>SummaryInformation 屬性

[**安裝程式**](installer-object.md)物件的 **SummaryInformation** 屬性會傳回 [**SummaryInfo**](summaryinfo-object.md)物件，此物件可用來檢查、更新和加入屬性至封裝或轉換的摘要資訊資料流程中。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如果使用大於0的 *maxProperties* 值來開啟現有的摘要資訊資料流程，就必須在關閉物件之前呼叫 [**保存**](summaryinfo-persist.md) 方法。 若無法這樣做，將會失去現有的資料流程資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




