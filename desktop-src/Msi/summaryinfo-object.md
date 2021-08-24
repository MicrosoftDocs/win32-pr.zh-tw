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
ms.openlocfilehash: 3efdc009f40f0bce67559d185afb4cba1289c00fc1d7771a43d392601220dbae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039588"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo 定義為 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SummaryInformation 屬性 (資料庫物件)**](database-summaryinformation.md)
</dt> <dt>

[**SummaryInformation 屬性 (安裝程式物件)**](installer-summaryinformation.md)
</dt> <dt>

[Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




