---
description: 提供提供瀏覽器設定的方法。 只有在 Windows XP 和 Windows Server 2003 上才支援 IItemPreviewerExt 介面，且不應再使用。
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: IItemPreviewerExt 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943278"
---
# <a name="iitempreviewerext-interface"></a>IItemPreviewerExt 介面

提供提供瀏覽器設定的方法。 只有在 Windows XP 和 Windows Server 2003 上才支援 **IItemPreviewerExt** 介面，且不應再使用。

## <a name="members"></a>成員

**IItemPreviewerExt** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IItemPreviewerExt** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IItemPreviewerExt** 介面具有這些方法。



| 方法                                                                               | 描述                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)               | 允許延伸至屬性的豐富內容。 <br/>                            |
| [**GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)                   | 取得要內嵌至輸出 MHTML 資料流程的相關主體部分。<br/>              |
| [**ProcessTransformCommand**](-search-iitempreviewerext-processtransformcommand.md) | 允許處理在預覽範本中遇到的轉換命令。<br/> |
| [**SuggestBrowserPolicy**](-search-iitempreviewerext-suggestbrowserpolicy.md)       | 建議要套用至瀏覽器的安全性原則。<br/>                        |



 

## <a name="remarks"></a>備註

只有在 Windows XP 和 Windows Server 2003 上才支援 **IItemPreviewerExt** 介面，且不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **IItemPreviewerExt** 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>          |



 

 
