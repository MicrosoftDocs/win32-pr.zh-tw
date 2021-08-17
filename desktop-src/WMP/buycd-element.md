---
title: BuyCD 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |BuyCD 元素
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- BuyCD 元素 Windows Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0b2af0f12b06c7d5701db3fcc073d7b7c330e8798408206b64a8b9811f27d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135841"
---
# <a name="buycd-element"></a>BuyCD 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**BuyCD** 元素會指定當使用者選擇進行購買時，Windows Media Player 顯示的網頁 url。

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (必要) 
</dt> <dd>

線上商店所顯示的網頁 URL，以提供 CD 或 DVD 供 Windows Media Player 購買。

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

線上商店顯示的網頁 URL，可在 Windows XP Media Center Edition 2004 更新中提供 CD 或 DVD 購買。

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

線上商店顯示的網頁 URL，可在另一個瀏覽器視窗中提供要購買的 CD 或 DVD。 Windows XP Service Pack 2 或更新版本也會使用此 URL 來取得「**線上購物音樂**」功能。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

當使用者按一下 Windows Media Player 中的按鈕或連結來購買 CD 或 DVD 時，播放 ServiceTask1 會將 URL 要求傳送給使用問號 (？ ) 查詢字串分隔符號所附加的參數。 下表詳細說明以 URL 要求傳送的參數。 其他可能存在於舊版相容性的用途。



| 名稱         | 值                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *專輯*      | 媒體專案之 **WM/AlbumTitle** 屬性的值。                                                                                                        |
| *演出者*     | **WM/AlbumArtist** 屬性的值（如果有的話），否則為媒體專案的 **Author** 屬性值。                                         |
| *大地 水準面*      | Windows 的地理位置識別碼。 在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。 |
| *locale*     | Windows Media Player 地區設定識別碼。                                                                                                                                     |
| *標題*      | 媒體專案的 **標題** 屬性值。                                                                                                                |
| *UFID*       | 媒體專案之 **WM/UniqueFileIdentifier** 屬性的值。                                                                                              |
| *userlocale* | Windows 地區設定識別碼。 地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。        |
| *version*    | 使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。                                                                         |



 

WindowsXP Media Center Edition 2004 提供使用者介面，其設計目的是要在某個距離觀看。 您應該針對要在大型顯示器上查看的 *MediaCenterURL* 參數建立網頁。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





