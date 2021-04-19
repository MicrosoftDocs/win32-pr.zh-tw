---
description: 資料庫物件的 SummaryInformation 屬性會傳回 SummaryInfo 物件，此物件可用來檢查、更新和加入屬性至摘要資訊資料流程。
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: SummaryInformation 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000484"
---
# <a name="databasesummaryinformation-property"></a>SummaryInformation 屬性

[**資料庫**](database-object.md)物件的 **SummaryInformation** 屬性會傳回 [**SummaryInfo**](summaryinfo-object.md)物件，此物件可用來檢查、更新和加入屬性至 [摘要資訊資料流程](summary-information-stream.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>屬性值

要加入或修改之屬性的最大數目。 這個參數是必要參數，可用來在串流產生期間配置足夠的工作記憶體。 不需要儲存此屬性數目。 如果資料庫是開啟唯讀，以防止更新資料流程，就必須使用零值。

## <a name="remarks"></a>備註

如果使用大於0的 *maxProperties* 值來開啟現有的摘要資訊資料流程，就必須在關閉物件之前呼叫 [**保存**](summaryinfo-persist.md) 方法。 若無法這樣做，將會遺失現有的資料流程資訊。

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




