---
description: 提供方法來定義使用者介面 (UI) 和索引子所建立之搜尋命名空間物件之間的互動。
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: ISearchItem 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386126"
---
# <a name="isearchitem-interface"></a>ISearchItem 介面

提供方法來定義使用者介面 (UI) 和索引子所建立之搜尋命名空間物件之間的互動。

## <a name="members"></a>成員

**ISearchItem** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ISearchItem** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISearchItem** 介面具有這些方法。



| 方法                                                         | 描述                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | 如果 URL 代表實際的 Shell 資料來源 (也稱為 Shell 命名空間延伸) ，則取得 **ISearchItem** 物件。<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | 取得 **ISearchItem** 的使用者介面 (UI) 物件。<br/>                                                                        |



 

## <a name="remarks"></a>備註

只有在 Windows XP 和 Windows Server 2003 上才支援 [**ISearchItem：： GetParentFolder**](-search-isearchitem-getparentfolder.md) ，且不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **ISearchItem** 介面和下列 Api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchProtocolUI**](-search-isearchprotocolui.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>          |



 

 
