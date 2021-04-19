---
description: CBaseWindow 類別是用來管理 windows 的基類。
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: 'CBaseWindow 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 313f1b222f3b0096d3f5bf92c15e2097afb29848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994914"
---
# <a name="cbasewindow-class"></a>CBaseWindow 類別

`CBaseWindow`類別是用來管理 windows 的基類。 影片轉譯器可以使用此類別來建立影片視窗。 若要使用這個類別，請建立繼承自的衍生類別 `CBaseWindow` 。 在衍生類別中：

-   執行可定義視窗樣式的純虛擬方法 [**CBaseWindow：： GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)。
-   覆寫處理視窗訊息的 [**CBaseWindow：： OnReceiveMessage**](cbasewindow-onreceivemessage.md) 方法。
-   執行可呼叫 [**CBaseWindow：:D onewithwindow**](cbasewindow-donewithwindow.md) 方法的函式。

使用衍生類別的實例之前，請先呼叫 [**CBaseWindow：:P reparewindow**](cbasewindow-preparewindow.md) 方法。



| 受保護的成員變數                                           | Description                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**m \_ hInstance**](cbasewindow-m-hinstance.md)                      | 模組實例的控制碼。                                                 |
| [**m \_ hwnd**](cbasewindow-m-hwnd.md)                                | 物件視窗的控制碼。                                                 |
| [**m \_ hdc**](cbasewindow-m-hdc.md)                                  | 視窗的裝置內容控制碼。                                         |
| [**m \_ 寬度**](cbasewindow-m-width.md)                              | 工作區的寬度（以圖元為單位）。                                           |
| [**m \_ 高度**](cbasewindow-m-height.md)                            | 用戶端區域的高度（以圖元為單位）。                                          |
| [**m \_ bActivated**](cbasewindow-m-bactivated.md)                    | 指定是否已啟用視窗的旗標。                     |
| [**m \_ pClassName**](cbasewindow-m-pclassname.md)                    | 包含視窗類別名稱的靜態字串。                      |
| [**m \_ ClassStyles**](cbasewindow-m-classstyles.md)                  | 視窗的類別樣式。                                                   |
| [**m \_ WindowStyles**](cbasewindow-m-windowstyles.md)                | 視窗的視窗樣式。                                                  |
| [**m \_ WindowStylesEx**](cbasewindow-m-windowstylesex.md)            | 視窗的延伸視窗樣式。                                         |
| [**m \_ ShowStageMessage**](cbasewindow-m-showstagemessage.md)        | 將視窗帶入前景的私用訊息。                      |
| [**m \_ ShowStageTop**](cbasewindow-m-showstagetop.md)                | 將視窗樣式設定為 WS \_ EX 最上層的私用訊息 \_ 。                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | 認識調色板的私用訊息。                                     |
| [**m \_ MemoryDC**](cbasewindow-m-memorydc.md)                        | 記憶體裝置內容的控制碼。                                           |
| [**m \_ hPalette**](cbasewindow-m-hpalette.md)                        | 視窗調色板的控制碼。                                                |
| [**m \_ bNoRealize**](cbasewindow-m-bnorealize.md)                    | 旗標，指定視窗是否應該實現其調色板。             |
| [**m \_ bBackground**](cbasewindow-m-bbackground.md)                  | 旗標，指定調色板是否應為背景調色板。        |
| [**m \_ bRealizing**](cbasewindow-m-brealizing.md)                    | 旗標，指定是否要實現新的調色板。                   |
| [**m \_ WindowLock**](cbasewindow-m-windowlock.md)                    | 重要區段，用來序列化物件的存取權。                           |
| [**m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md)                        | 指定是否要取得裝置內容的旗標。                    |
| [**m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md)        | 指定視窗是否張貼或傳送其損毀訊息的旗標。 |
| 保護方法                                                    | Description                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | 處理調色板變更訊息。 虛擬。                                      |
| 公用方法                                                       | Description                                                                    |
| [**CBaseWindow**](cbasewindow-cbasewindow.md)                       | 函式方法。                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | 終結視窗。 虛擬。                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | 建立視窗。 虛擬。                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | 會視窗。 虛擬。                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | 根據衍生類別的需求，調整視窗的大小。 虛擬。  |
| [**OnSize**](cbasewindow-onsize.md)                                 | 處理 WM \_ 大小的訊息。 虛擬。                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | 處理 WM \_ 關閉訊息。 虛擬。                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | 抓取工作區的預設大小。 虛擬。                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | 釋放視窗的資源。 虛擬。                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | 初始化視窗。 虛擬。                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | 通知視窗，轉譯器的輸入釘已連接。          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | 建立視窗。                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | 將視窗對齊 **DWORD** 界限，以獲得最大效能。            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | 設定視窗的顯示狀態。                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | 導致重新繪製視窗。                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | 將視窗帶入前景。                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | 安裝視窗的調色板。 虛擬。                                    |
| [**SetRealize**](cbasewindow-setrealize.md)                         | 指定視窗是否發現調色板。                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | 認識視窗的目前調色板。 虛擬。                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | 讓衍生類別將訊息轉送到另一個視窗。 虛擬。        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | 抓取視窗的目前寬度。                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | 抓取視窗目前的高度。                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | 抓取視窗的控制碼。                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | 抓取記憶體裝置內容的控制碼。                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | 抓取視窗的裝置內容控制碼。                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | 處理視窗訊息。 虛擬。                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | 刪除視窗目前的調色板，並還原預設的系統調色板。  |
| 純虛擬方法                                                 | Description                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | 抓取視窗的類別樣式和視窗樣式。                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




