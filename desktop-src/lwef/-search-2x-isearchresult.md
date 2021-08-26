---
title: 'ISearchResult 介面 (WdsSharedIDL .h) '
description: 公開有關結果集的資訊和屬性。
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- ISearchResult 介面舊版 Windows 環境功能
- ISearchResult 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd15db1340b28c8ac273746a64a5aee8c4b3235155d948692ffcc16582ac4549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963518"
---
# <a name="isearchresult-interface"></a>ISearchResult 介面

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

公開有關結果集的資訊和屬性。

## <a name="members"></a>成員

**ISearchResult** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ISearchResult** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISearchResult** 介面具有這些方法。



| 方法                                                            | 描述                 |
|:------------------------------------------------------------------|:----------------------------|
| [**可用性**](-search-2x-isearchresult-availability.md)     | 未實作。<br/> |
| [**DoVerb**](-search-2x-isearchresult-doverb.md)                 | 未實作。<br/> |
| [**GetIcon**](-search-2x-isearchresult-geticon.md)               | 未實作。<br/> |
| [**GetThumbnail**](-search-2x-isearchresult-getthumbnail.md)     | 未實作。<br/> |
| [**GetValue**](-search-2x-isearchresult-getvalue.md)             | 未實作。<br/> |
| [**GetVerb**](-search-2x-isearchresult-getverb.md)               | 未實作。<br/> |
| [**IconCount**](-search-2x-isearchresult-iconcount.md)           | 未實作。<br/> |
| [**索引**](-search-2x-isearchresult-index.md)                   | 未實作。<br/> |
| [**LoadState**](-search-2x-isearchresult-loadstate.md)           | 未實作。<br/> |
| [**預覽程式**](-search-2x-isearchresult-previewer.md)           | 未實作。<br/> |
| [**PutValue**](-search-2x-isearchresult-putvalue.md)             | 未實作。<br/> |
| [**ThumbnailState**](-search-2x-isearchresult-thumbnailstate.md) | 未實作。<br/> |
| [**類型**](-search-2x-isearchresult-type.md)                     | 未實作。<br/> |
| [**VerbCount**](-search-2x-isearchresult-verbcount.md)           | 未實作。<br/> |



 

## <a name="remarks"></a>備註

這些方法會公開適用于結果集的屬性和動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>                                               |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

