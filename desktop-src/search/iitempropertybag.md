---
description: 定義方法，以取得搜尋專案屬性的相關資訊。 只有 Windows XP 和 Windows Server 2003 才支援此介面，因此不應再使用。
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: IItemPropertyBag 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2657fea53c4e7021e17df4b74cc210bd8547180566ff579524f85b7663a0c247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226559"
---
# <a name="iitempropertybag-interface"></a>IItemPropertyBag 介面

定義方法，以取得搜尋專案屬性的相關資訊。 只有 Windows XP 和 Windows Server 2003 才支援此介面，因此不應再使用。

## <a name="members"></a>成員

**IItemPropertyBag** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IItemPropertyBag** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IItemPropertyBag** 介面具有這些方法。



| 方法                                                      | 描述                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | 取得屬性包中屬性數目的計數。<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | 取得讀取或儲存屬性包中的屬性所需的資訊。<br/> |
| [**讀**](iitempropertybag-read.md)                       | 使一或多個屬性從屬性包中讀取。<br/>                   |
| [**寫**](iitempropertybag-write.md)                     | 導致一或多個屬性儲存在屬性包中。<br/>                  |



 

## <a name="remarks"></a>備註

只有 Windows XP 和 Windows Server 2003 才支援 **IItemPropertyBag** 介面，因此不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **IItemPropertyBag** 介面和下列 api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPreviewerExt**](-search-iitempreviewerext.md)和 [**ISearchItem**](-search-isearchitem.md)介面、 [**LINKINFO**](-search-linkinfo.md)和 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop)結構，以及 [**LINKTYPE**](-search-linktype.md)列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>          |



 

 
