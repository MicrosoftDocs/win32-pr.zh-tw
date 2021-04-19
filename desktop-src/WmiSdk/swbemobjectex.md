---
description: 提供 SWbemObject 的擴充功能。 如同 SWbemObject，所有的 WMI 物件都可以使用此擴充物件的方法。
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: 'SWbemObjectEx 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: abed8c1d58687203aaeb32918cf15b2785b92622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997110"
---
# <a name="swbemobjectex-object"></a>SWbemObjectEx 物件

**SWbemObjectEx** 物件提供 [**SWbemObject**](swbemobject.md)的擴充功能。 如同 **SWbemObject**，所有的 WMI 物件都可以使用此擴充物件的方法。 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。

## <a name="members"></a>成員

**SWbemObjectEx** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemObjectEx** 物件有這些方法。



| 方法                                      | 描述                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [**GetText\_**](swbemobjectex-gettext-.md) | 傳回文字檔，此文字檔會以 XML 顯示物件的內容。<br/> |
| [**重新整理\_**](swbemobjectex-refresh-.md) | 重新整理物件中的資料。<br/>                                  |
| **SetFromText\_**                           | 保留供未來使用。<br/>                                      |



 

### <a name="properties"></a>屬性

**SWbemObjectEx** 物件具有這些屬性。



| 屬性                                                                 | 存取類型           | Description                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SystemProperties\_**](swbemobjectex-systemproperties-.md)<br/> | 讀取/寫入<br/> | [**內含**](swbempropertyset.md)物件，其中包含適用于 **SWbemObjectEx** 的系統屬性集合。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[WbemObjectTextFormatEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

