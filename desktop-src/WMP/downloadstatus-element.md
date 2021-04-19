---
title: 'DownloadStatus 元素 (Msfeeds) '
description: '請注意，本節將說明針對線上商店使用而設計的功能。 |DownloadStatus 元素 (Msfeeds) '
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- DownloadStatus 元素 Windows Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987172"
---
# <a name="downloadstatus-element"></a>DownloadStatus 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**DownloadStatus** 元素會指定 Windows Media Player 顯示為連結的 URL，讓使用者能夠查看下載狀態。

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="URL"></span><span id="url"></span>Url
</dt> <dd>

線上商店顯示的網頁 URL，可向使用者顯示下載狀態。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

Windows Media Player 會在下載進行時向使用者顯示訊息。 如果目前作用中的服務定義了下載狀態 URL，使用者可以按一下郵件內文。 當使用者按一下訊息時，播放程式會流覽至 **DownloadStatus** 元素所指定的 URL，讓目前的使用中存放區可以提供進行中下載的詳細資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/>                                          |
| 標頭<br/>  | <dl> <dt>Msfeeds。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





