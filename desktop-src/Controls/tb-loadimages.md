---
title: 'TB_LOADIMAGES 訊息 (Commctrl .h) '
description: 將系統定義的按鈕影像載入工具列控制項的影像清單。
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df2cfae5e1658dec2652eb68cae4283dd0df697ad055434f1290cc0da7c2b485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168194"
---
# <a name="tb_loadimages-message"></a>TB \_ LOADIMAGES 訊息

將系統定義的按鈕影像載入工具列控制項的影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

系統定義之按鈕影像清單的識別碼。 這個參數可以設定為下列其中一個值。



| 值                                                                                                                                                                                | 意義                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**.IDB \_ >HIST \_ 大型 \_ 色彩**</dt> </dl> | WindowsExplorer 點陣圖大小很大。<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**.IDB \_ >HIST \_ 小型 \_ 色彩**</dt> </dl> | WindowsExplorer 點陣圖的大小很小。<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**.IDB \_ STD \_ 大型 \_ 色彩**</dt> </dl>    | 大小較大的標準點陣圖。<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**.IDB \_ STD \_ SMALL \_ COLOR**</dt> </dl>    | 小型的標準點陣圖。<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**.IDB \_ 視圖 \_ 大型 \_ 色彩**</dt> </dl> | 以大尺寸觀看點陣圖。<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**.IDB \_ 視圖 \_ 小 \_ 色彩**</dt> </dl> | 以小尺寸觀看點陣圖。<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**\_>HIST \_ 一般的 .IDB**</dt> </dl>                 | WindowsExplorer 行進按鈕和處於正常狀態的我的最愛點陣圖。<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**\_>HIST \_ 熱的 .IDB**</dt> </dl>                          | Windows處於作用中狀態的 Explorer 行進按鈕和我的最愛點陣圖。<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**\_ \_ 已停用 .IDB >HIST**</dt> </dl>           | Windows已停用狀態的 Explorer 行進按鈕和我的最愛點陣圖。<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**已 \_ 按下的 .IDB >HIST \_**</dt> </dl>              | WindowsExplorer 行進按鈕和按下的我的最愛點陣圖。<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

實例控制碼。 此參數必須設定為 HINST \_ COMMCTRL。

</dd> </dl>

## <a name="return-value"></a>傳回值

影像清單中的影像計數。 如果工具列沒有影像清單，或現有的影像清單是空的，則傳回零。

## <a name="remarks"></a>備註

當您在傳送 [**TB \_ ADDBUTTONS**](tb-addbuttons.md)訊息之前準備 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構時，必須使用適當的映射索引值。 如需這些預設點陣圖的影像索引值清單，請參閱 [工具列標準按鈕影像索引值](toolbar-standard-button-image-index-values.md)。

## <a name="examples"></a>範例

下列範例程式碼會載入系統標準的小型色彩影像。


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





