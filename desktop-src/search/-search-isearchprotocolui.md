---
description: 提供叫用 ISearchItem 物件的方法。
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: ISearchProtocolUI 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4794c0a2de43c08645af5ea7d44d0dbd872fe6fc88c33f5fcdb830955fc594be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463013"
---
# <a name="isearchprotocolui-interface"></a>ISearchProtocolUI 介面

提供叫用 [**ISearchItem**](-search-isearchitem.md) 物件的方法。 當處理來自收集程式的 Url 時，通訊協定主機會呼叫此介面中的方法。 通訊協定處理常式會執行以原生格式存取內容來源的通訊協定，而此介面會執行自訂的通訊協定處理常式，以展開可編制索引的資料來源。

## <a name="members"></a>成員

**ISearchProtocolUI** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ISearchProtocolUI** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISearchProtocolUI** 介面具有這些方法。



| 方法                                                                       | 描述                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | 取得指定之資料的搜尋專案。 針對收集程式所處理的每個 URL，會呼叫這個方法一次，並抓取 [**ISearchItem**](-search-isearchitem.md) 物件的指標。 <br/> |



 

## <a name="remarks"></a>備註

只有 Windows XP 和 Windows Server 2003 才支援 **ISearchProtocolUI** 介面，因此不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **ISearchProtocolUI** 介面和下列 api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchItem**](-search-isearchitem.md)介面、 [**LINKINFO**](-search-linkinfo.md)結構和 [**LINKTYPE**](-search-linktype.md)列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>          |



 

 
