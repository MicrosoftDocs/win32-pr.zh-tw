---
title: 'DPI_AWARENESS_CONTEXT 處理 (windef .h) '
description: 識別視窗的感知內容。
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317276"
---
# <a name="dpi_awareness_context-handle"></a>DPI \_ 感知 \_ 內容控制碼

識別視窗的感知內容。

## <a name="syntax"></a>Syntax

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>常數

**DPI \_ 感知 \_ 內容未 \_ 察覺**<dl> 不知道 DPI。 此視窗不會針對 DPI 變更進行調整，而且一律會假設其比例因數為 100% (96 DPI) 。 系統會自動以任何其他 DPI 設定來調整它的規模。  
</dl>

**DPI \_ 感知 \_ 內容 \_ 系統 \_ 感知**<dl> 系統 DPI 感知。 此視窗不會針對 DPI 變更進行調整。 它會查詢 DPI 一次，並在進程的存留期內使用該值。 如果 DPI 變更，進程將不會調整為新的 DPI 值。 當系統值的 DPI 變更時，系統會自動相應增加或減少系統的規模。  
</dl>

**\_ \_ \_ 感知每個 \_ 監視器 \_ 的 DPI 感知內容**<dl> 每個監視器 DPI 感知。 此視窗會在建立時檢查 DPI，並在每次 DPI 變更時調整比例因數。 系統不會自動調整這些處理常式。  
</dl>

**\_ \_ 每個監視器的 DPI 感知內容 \_ \_ \_ 感知 \_ V2**<dl> 也稱為 **每個監視器 v2**。 優於原始的個別監視器 DPI 感知模式，可讓應用程式在每個最上層視窗上存取新的 DPI 相關縮放行為。  
在 Windows 10 的建立者更新中提供每個監視器 v2，而且在舊版的作業系統上無法使用。  
引進的其他行為如下：

-   **子視窗 DPI 變更通知** -在每個監視器 v2 內容中，整個視窗樹狀結構會在發生的任何 DPI 變更時收到通知。
-   **縮放非工作區** -所有視窗都會自動以 DPI 敏感性的方式繪製其非工作區。 不需要呼叫 [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) 。
-   **Win32 功能表的調整** -每個監視器 v2 內容中建立的所有 ntuser.man 功能表都會以每個監視器的方式調整。
-   **對話方塊縮放** -在每個監視器中建立的 Win32 對話方塊會自動回應 DPI 變更。
-   **改善 comctl32.dll 控制項的縮放比例** -各種 comctl32.dll 控制項都已改善每個監視器 v2 內容中的 DPI 縮放行為。
-   **改善的主題行為** -在每個監視器 v2 視窗的內容中開啟的 UxTheme 控制碼，將會以與該視窗相關聯的 DPI 來運作。

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

以 GDI 為基礎的內容改善品質的 DPI 感知。 這種模式的行為類似于 DPI_AWARENESS_CONTEXT_UNAWARE，但也可讓系統在高 DPI 監視器上顯示視窗時，自動改善文字轉譯品質和其他以 GDI 為基礎的基本類型。

如需更多詳細資訊，請參閱 [改善以 GDI 為基礎的桌面應用程式中的高 DPI 體驗](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97)。

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED 于2018年10月的更新中引進 Windows 10 (也稱為1809版) 。


## <a name="requirements"></a>規格需求

| 需求 | 值 |
|----|-----------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1607版桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援 <br/>  |
| 標頭<br/>                   | <dl> <dt>windef。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AreDpiAwarenessCoNtextsEqual**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**GetAwarenessFromDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**GetDpiFromDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**GetThreadDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**GetWindowDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**IsValidDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**SetProcessDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**SetThreadDpiAwarenessCoNtext**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
