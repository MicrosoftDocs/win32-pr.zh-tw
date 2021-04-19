---
description: SummaryInfo 物件是用來讀取、建立和更新儲存物件之摘要資訊資料流程中的檔案屬性。
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: SummaryInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985773"
---
# <a name="summaryinfo-object"></a>SummaryInfo 物件

**SummaryInfo** 物件是用來讀取、建立和更新儲存物件之 [摘要資訊資料流程](summary-information-stream.md)中的檔案屬性。

## <a name="members"></a>成員

**SummaryInfo** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SummaryInfo** 物件有這些方法。



| 方法                                 | 描述                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**堅持**](summaryinfo-persist.md) | 將先前儲存的屬性格式化並寫入標準 [摘要資訊資料流程](summary-information-stream.md)中。<br/> |



 

### <a name="properties"></a>屬性

**SummaryInfo** 物件具有這些屬性。



| 屬性                                                                             | 描述                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**屬性屬性 (SummaryInfo 物件)**](summaryinfo-summaryinfo.md)<br/> | 取得或設定摘要資訊資料流程中指定之屬性的值。<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | 表示摘要資訊物件中目前的屬性值數目。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo 定義為 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SummaryInformation 屬性 (資料庫物件)**](database-summaryinformation.md)
</dt> <dt>

[**SummaryInformation 屬性 (安裝程式物件)**](installer-summaryinformation.md)
</dt> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




