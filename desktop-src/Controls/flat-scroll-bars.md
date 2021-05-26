---
title: 平面捲軸
description: Microsoft Internet Explorer 4.0 推出了一個新的視覺技術，稱為「一般捲軸」。
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423888"
---
# <a name="flat-scroll-bars"></a>平面捲軸

Microsoft Internet Explorer 4.0 推出了一個新的視覺技術，稱為「一般捲軸」。 功能上，一般捲軸的行為就像標準捲軸。 不同之處在于，您可以自訂其外觀，以比標準捲軸更大的範圍。

下圖顯示包含平面捲軸的視窗。

![包含平面捲軸之視窗的螢幕擷取畫面](images/flatsb.jpg)

> [!Note]  
> Comctl32.dll 版本4.71 至5.82 支援平面捲軸。 Comctl32.dll 6.00 版和更新版本不支援一般捲軸。

 

## <a name="using-flat-scroll-bars"></a>使用平面捲軸

本節說明如何在您的應用程式中執行平面捲軸。

### <a name="before-you-begin"></a>開始之前

若要使用一般捲軸函式，您必須在原始程式檔中包含 Commctrl，並連結至 Comctl32.dll。

### <a name="adding-flat-scroll-bars-to-a-window"></a>將平面捲軸加入至視窗

若要將一般捲軸加入至視窗，請呼叫 [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)，並將控制碼傳遞至視窗。 您必須使用對等的 FlatSB XXX 函式，而不是使用標準捲軸函數來操作捲軸 \_ 。 有一些一般捲軸函式，可用於設定和取出捲軸資訊、範圍和位置。 如果您的視窗尚未初始化一般捲軸，則一般捲軸 API 會延後至對應的標準函式（如果使用的話）。 這可讓您開啟和關閉平面捲軸，而不需要撰寫條件式程式碼。

由於應用程式可能已為其平面捲軸設定自訂計量，因此系統計量變更時不會自動更新。 當系統捲軸計量變更時，會廣播 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) 訊息，並將其 *wParam* 設定為 [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)。 若要將一般捲軸更新為新的系統計量，應用程式必須處理這個訊息，並明確地變更一般捲軸的度量相依屬性。

若要更新您的捲軸屬性，請使用 [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop)。 下列程式碼片段會將一般捲軸的度量相依屬性變更為目前的系統值。


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a>強化平面捲軸

[**FlatSB \_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) 可讓您修改一般捲軸，以自訂視窗的外觀。 若為垂直捲動條，您可以變更橫條的寬度和方向箭號的高度。 針對水準捲軸，您可以變更橫條的高度和方向箭號的寬度。 您也可以變更水準和垂直捲動條的背景色彩。

[**FlatSB \_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) 也可讓您自訂如何顯示一般捲軸。 藉由變更 WSB \_ \_ 屬性 VSTYLE 和 wsb \_ \_ 屬性 HSTYLE 屬性，您可以設定要使用的捲軸類型。 有三種樣式可供使用。



|   樣式                 |   描述                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FSB \_ 百科全書 \_ 模式 | 標準的平面捲軸隨即顯示。 當滑鼠移到方向按鈕或 thumb 上方時，捲軸的那個部分會顯示在3-d 中。             |
| 前端匯流排 \_ 平面 \_ 模式    | 標準的平面捲軸隨即顯示。 當滑鼠移到方向按鈕或 thumb 上方時，捲軸的那個部分會以反轉色彩顯示。 |
| FSB \_ 一般 \_ 模式 | 隨即顯示一般的 nonflat 捲軸。 不會套用任何特殊的視覺效果。                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>移除一般捲軸

如果您想要從視窗中移除一般捲軸，請呼叫 [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) 函式，並將控制碼傳遞至視窗。 此函數只會在執行時間從視窗中移除一般捲軸。 當您的視窗損毀時，您不需要呼叫此函式。

 

 