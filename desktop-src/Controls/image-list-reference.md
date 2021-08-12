---
title: 影像清單
description: 本章節包含與影像清單搭配使用之程式設計項目的相關資訊。
ms.assetid: 8a2bdc59-747c-47bb-b125-9b0b97af205e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a9a24bfda9156fc3e84cece4c7710ab42d9c9766578bb2c3bde6809b246292
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672103"
---
# <a name="image-lists"></a>影像清單

本章節包含與影像清單搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                          | 目錄                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [影像清單](image-lists.md) | 影像清單是相同大小的影像集合，每個影像都可由其索引參考。<br/> |



 

### <a name="functions"></a>函式



| 主題                                                                 | 目錄                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HIMAGELIST \_ QueryInterface**](/windows/desktop/api/Commctrl/nf-commctrl-himagelist_queryinterface)       | 抓取 [**IImageList**](/windows/desktop/api/CommonControls/nn-commoncontrols-iimagelist) 或 [**IImageList2**](/windows/desktop/api/Commoncontrols/nn-commoncontrols-iimagelist2) 物件的指標，該物件對應至影像清單的 HIMAGELIST 控制碼。<br/>                                                                                                           |
| [**ImageList \_ 新增**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add)                               | 將影像或影像加入至影像清單。 <br/>                                                                                                                                                                                                                                |
| [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)                   | 將影像或影像加入至影像清單，從指定的點陣圖產生遮罩。<br/>                                                                                                                                                                                    |
| [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)                   | 開始拖曳影像。 <br/>                                                                                                                                                                                                                                                |
| [**ImageList \_ CoCreateInstance**](/windows/desktop/api/CommonControls/nf-commoncontrols-imagelist_cocreateinstance)     | 建立 imagelist 的單一實例，並傳回其介面指標。<br/>                                                                                                                                                                                         |
| [**ImageList \_ 複製**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_copy)                             | 複製指定影像清單中的影像。 <br/>                                                                                                                                                                                                                                 |
| [**ImageList \_ 建立**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)                         | 建立新的影像清單。 <br/>                                                                                                                                                                                                                                                |
| [**ImageList 損 \_ 毀**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy)                       | 終結影像清單。<br/>                                                                                                                                                                                                                                                   |
| [**ImageList \_ system.windows.dragdrop.dragenter>**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter)                   | 在視窗中的指定位置顯示拖曳影像。 <br/>                                                                                                                                                                                                     |
| [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave)                   | 解除鎖定指定的視窗並隱藏拖曳影像，讓視窗得以更新。 <br/>                                                                                                                                                                                |
| [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)                     | 移動在拖放作業期間正在拖曳的影像。 通常會呼叫此函式來回應 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。 <br/>                                                                                           |
| [**ImageList \_ DragShowNolock**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragshownolock)         | 顯示或隱藏正在拖曳的影像。 <br/>                                                                                                                                                                                                                                  |
| [**ImageList \_ 繪圖**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw)                             | 在指定的裝置內容中繪製影像清單專案。 <br/>                                                                                                                                                                                                                |
| [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex)                         | 在指定的裝置內容中繪製影像清單專案。 此函式會使用指定的繪製樣式，並將影像與指定的色彩混合。 <br/>                                                                                                                   |
| [**ImageList \_ DrawIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawindirect)             | 根據 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) 結構繪製影像清單影像。 <br/>                                                                                                                                                                      |
| [**ImageList \_ 重複**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_duplicate)                   | 建立現有影像清單的複本。 <br/>                                                                                                                                                                                                                           |
| [**ImageList \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag)                       | 結束拖曳作業。 <br/>                                                                                                                                                                                                                                                   |
| [**ImageList \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor)                 | 抓取影像清單目前的背景色彩。 <br/>                                                                                                                                                                                                                |
| [**ImageList \_ GetDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage)             | 抓取用於拖曳影像的暫存影像清單。 函式也會擷取目前拖曳位置以及拖曳影像相對於拖曳位置的位移。 <br/>                                                                                |
| [**ImageList \_ GetIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon)                       | 從影像和影像清單中的遮罩建立圖示。 <br/>                                                                                                                                                                                                                 |
| [**ImageList \_ GetIconSize**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticonsize)               | 抓取影像清單中的影像維度。 影像清單中的所有影像都有相同的維度。 <br/>                                                                                                                                                               |
| [**ImageList \_ GetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount)           | 抓取影像清單中的影像數目。 <br/>                                                                                                                                                                                                                         |
| [**ImageList \_ GetImageInfo**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo)             | 抓取影像的相關資訊。 <br/>                                                                                                                                                                                                                                    |
| [**ImageList \_ LoadImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_loadimagea)                   | 從指定的點陣圖建立影像清單。<br/>                                                                                                                                                                                                                          |
| [**ImageList \_ 合併**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge)                           | 藉由結合兩個現有的影像來建立新的映射。 函式也會建立用來儲存影像的新影像清單。 <br/>                                                                                                                                            |
| [**ImageList \_ 讀取**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_read)                             | 從資料流程讀取影像清單。 <br/>                                                                                                                                                                                                                                       |
| [**ImageList \_ ReadEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_readex)                         | 從資料流程讀取影像清單，並將介面傳回到影像清單。 <br/>                                                                                                                                                                                           |
| [**ImageList \_ 移除**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove)                         | 從影像清單中移除影像。 <br/>                                                                                                                                                                                                                                     |
| [**ImageList \_ 取代**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace)                       | 以新的影像取代影像清單中的影像。 <br/>                                                                                                                                                                                                                     |
| [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon)               | 以圖示或游標取代影像。<br/>                                                                                                                                                                                                                                 |
| [**ImageList \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor)                 | 設定影像清單的背景色彩。 只有當您新增圖示或使用具有黑色和白色點陣圖的 [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) 時，此函式才會運作。 如果沒有遮罩，則會繪製整個影像;因此，不會顯示背景色彩。 <br/> |
| [**ImageList \_ SetColorTable**](imagelist-setcolortable.md)           | 設定影像清單的色彩表。<br/>                                                                                                                                                                                                                                   |
| [**ImageList \_ SetDragCursorImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) | 藉由結合指定的影像 (通常是使用目前拖曳影像) 的滑鼠游標影像，來建立新的拖曳影像。 <br/>                                                                                                                                                  |
| [**ImageList \_ SetIconSize**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_seticonsize)               | 設定影像清單中的影像大小，並從清單中移除所有影像。 <br/>                                                                                                                                                                                     |
| [**ImageList \_ SetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setimagecount)           | 調整現有影像清單的大小。 <br/>                                                                                                                                                                                                                                          |
| [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage)       | 將指定的影像新增至要當做覆迭遮罩使用的影像清單。 在4.70 版和更舊版本中，影像清單最多可有四個覆迭遮罩，4.71 版中最多可以有15個。 函數會將覆迭遮罩索引指派給指定的影像。 <br/>                   |
| [**ImageList \_ 寫入**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_write)                           | 將影像清單寫入資料流程。 <br/>                                                                                                                                                                                                                                        |
| [**ImageList \_ WriteEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_writeex)                       | 將影像清單寫入資料流程。 <br/>                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>巨集



| 主題                                                   | 目錄                                                                                                                                                                         |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon)         | 將圖示或游標加入影像清單中。 [**ImageList \_AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) 會呼叫 [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) 函數。 <br/> |
| [**ImageList \_ ExtractIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_extracticon) | 呼叫 [**ImageList \_ GetIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) 函式，根據影像清單中的影像和遮罩來建立圖示或游標。 <br/>                          |
| [**ImageList \_ LoadBitmap**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_loadbitmap)   | 呼叫 [**ImageList \_ LoadImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_loadimagea) 函數，以從指定的點陣圖資源建立影像清單。 <br/>                                   |
| [**ImageList \_ RemoveAll**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_removeall)     | 呼叫 [**ImageList \_ remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) 函式，以移除影像清單中的所有影像。 <br/>                                                     |
| [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask)        | 準備覆迭遮罩的索引，讓 [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 函數可以使用它。 <br/>                                                     |



 

### <a name="interfaces"></a>介面



| 主題                            | 目錄                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IImageList**](/windows/desktop/api/CommonControls/nn-commoncontrols-iimagelist) | 公開操作和與影像清單互動的方法。 <br/> 若要使用 [**IImageList**](/windows/desktop/api/CommonControls/nn-commoncontrols-iimagelist)，請在資訊清單中指定 Comctl32.dll 第6版。 如果您沒有這麼做，預設會使用 Comctl32.dll 第5版， **IImageList** 可能會顯示無法預期的行為。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。<br/> |



 

### <a name="methods"></a>方法



| 主題                                                       | 目錄                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**加**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-add)                               | 將影像或影像加入至影像清單。<br/>                                                                                                                                                                                                                                                                |
| [**AddMasked**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-addmasked)                   | 將影像或影像加入至影像清單，從指定的點陣圖產生遮罩。 <br/>                                                                                                                                                                                                                  |
| [**BeginDrag**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-begindrag)                   | 開始拖曳影像。 <br/>                                                                                                                                                                                                                                                                               |
| [**複製**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-clone)                           | 複製現有的影像清單。 <br/>                                                                                                                                                                                                                                                                          |
| [**複製**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-copy)                             | 從指定的影像清單複製影像。 <br/>                                                                                                                                                                                                                                                                  |
| [**DragEnter**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-dragenter)                   | 在拖曳作業期間鎖定指定視窗的更新，並在視窗內的指定位置顯示拖曳影像。 <br/>                                                                                                                                                                  |
| [**DragLeave**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-dragleave)                   | 解除鎖定指定的視窗，並隱藏拖曳影像，讓視窗更新。 <br/>                                                                                                                                                                                                              |
| [**DragMove**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-dragmove)                     | 移動在拖放作業期間正在拖曳的影像。 通常會呼叫此函式來回應 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息。 <br/>                                                                                                                          |
| [**DragShowNolock**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-dragshownolock)         | 顯示或隱藏正在拖曳的影像。 <br/>                                                                                                                                                                                                                                                                 |
| [**Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw)                             | 在指定的裝置內容中繪製影像清單專案。 <br/>                                                                                                                                                                                                                                               |
| [**EndDrag**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-enddrag)                       | 結束拖曳作業。 <br/>                                                                                                                                                                                                                                                                                  |
| [**GetBkColor**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getbkcolor)                 | 取得影像清單目前的背景色彩。 <br/>                                                                                                                                                                                                                                                    |
| [**GetDragImage**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getdragimage)             | 取得用於拖曳影像的暫存影像清單。 函式也會擷取目前拖曳位置以及拖曳影像相對於拖曳位置的位移。 <br/>                                                                                                                    |
| [**GetIcon**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-geticon)                       | 從影像和影像清單中的遮罩建立圖示。 <br/>                                                                                                                                                                                                                                              |
| [**GetIconSize**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-geticonsize)               | 取得影像清單中影像的維度。 影像清單中的所有影像都有相同的維度。 <br/>                                                                                                                                                                                                   |
| [**GetImageCount**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getimagecount)           | 取得影像清單中的影像數目。 <br/>                                                                                                                                                                                                                                                             |
| [**GetImageInfo**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getimageinfo)             | 取得影像的相關資訊。 <br/>                                                                                                                                                                                                                                                                        |
| [**GetImageRect**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getimagerect)             | 取得影像的周框。 <br/>                                                                                                                                                                                                                                                                     |
| [**GetItemFlags**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getitemflags)             | 取得影像的旗標。<br/>                                                                                                                                                                                                                                                                              |
| [**GetOverlayImage**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getoverlayimage)       | 從當做覆迭遮罩的影像清單抓取指定的影像。 <br/>                                                                                                                                                                                                                              |
| [**合併**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-merge)                           | 藉由結合兩個現有的影像來建立新的映射。 這個方法也會建立用來儲存影像的新影像清單。 <br/>                                                                                                                                                                            |
| [**移除**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-remove)                         | 從影像清單中移除影像。 <br/>                                                                                                                                                                                                                                                                    |
| [**取代**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-replace)                       | 以新的影像取代影像清單中的影像。<br/>                                                                                                                                                                                                                                                     |
| [**ReplaceIcon**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-replaceicon)               | 以圖示或游標取代影像。 <br/>                                                                                                                                                                                                                                                               |
| [**SetBkColor**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-setbkcolor)                 | 設定影像清單的背景色彩。 只有在您將圖示加入影像清單中，或使用 [**IImageList：： AddMasked**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-addmasked) 方法來加入黑色和白色點陣圖時，此方法才有作用。 如果沒有遮罩，則會繪製整個影像，而不會顯示背景色彩。 <br/>  |
| [**SetDragCursorImage**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-setdragcursorimage) | 藉由結合指定的影像（通常是滑鼠游標影像）和目前的拖曳影像，來建立新的拖曳影像。 <br/>                                                                                                                                                                        |
| [**SetIconSize**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-seticonsize)               | 設定影像清單中的影像大小，並從清單中移除所有影像。 <br/>                                                                                                                                                                                                                    |
| [**SetImageCount**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-setimagecount)           | 調整現有影像清單的大小。 <br/>                                                                                                                                                                                                                                                                         |
| [**SetOverlayImage**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-setoverlayimage)       | 將指定的影像新增至用作覆迭遮罩的影像清單。 在通用控制項 [4.70 版](common-control-versions.md) 和更舊版本中，影像清單最多可有四個覆迭遮罩，4.71 版或更新版本中最多可以有15個。 方法會將覆迭遮罩索引指派給指定的影像。 <br/> |



 

### <a name="structures"></a>結構



| 主題                                              | 目錄                                                                                                                                                                |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMAGEINFO**](/windows/win32/api/commctrl/ns-commctrl-imageinfo)                     | 包含影像清單中之影像的相關資訊。 此結構會搭配 [**IImageList：： GetImageInfo**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-getimageinfo) 函數使用。 <br/> |
| [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) | 包含影像清單繪製作業的相關資訊，並與 [**IImageList：:D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) 函數搭配使用。 <br/>                          |



 

 

