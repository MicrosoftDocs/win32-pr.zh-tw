---
title: 關於 Rebar 控制項
description: Rebar 控制項作為子視窗的容器。
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d34f76ca745f0807b849bd7c42c81944f11e4429fe2dc9670fa318cbd575ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434820"
---
# <a name="about-rebar-controls"></a>關於 Rebar 控制項

*Rebar 控制項* 作為子視窗的容器。 它可以包含一個或多個 *區段*，而且每個波段都可以有任意組合的控制手柄列、點陣圖、文字標籤和一個子視窗。 應用程式會將子視窗（通常是另一個控制項）指派給 Rebar 控制區。 當您動態地重新放置 Rebar 控制區時，Rebar 控制項會管理指派給該頻外之子視窗的大小和位置。 此外，應用程式也可以指定寬線的背景點陣圖，而 Rebar 控制項將會透過點陣圖顯示寬線的子視窗。

下列螢幕擷取畫面顯示具有兩個帶的 Rebar 控制項。 其中一個包含工具列，另一個包含 combobox。 這兩個波段都有一個可讓他們移動和調整大小的移動控制。

![對話方塊的螢幕擷取畫面，其中顯示具有包含工具列和包含下拉式方塊之帶狀線的 Rebar 控制項](images/rb-rebar.png)

> [!Note]  
> Rebar 控制項是在 Comctl32.dll 4.70 版和更新版本中執行。

 

## <a name="rebar-bands-and-child-windows"></a>Rebar 區段和子 Windows

應用程式會使用 [**rb \_ INSERTBAND**](rb-insertband.md) 和 [**rb \_ SETBANDINFO**](rb-setbandinfo.md) 訊息來定義 Rebar 帶的特性。 這些訊息接受 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) 結構的位址做為 *lParam* 參數。 **REBARBANDINFO** 結構成員會定義指定之頻外的特性。 若要設定寬線的特性，請設定 **cbsize** 成員以表示結構的大小（以位元組為單位）。 然後設定 **fMask** 成員，以指出您的應用程式所要填入的結構成員。

若要將子視窗指派給頻外，請 \_ 在 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的 **FMASK** 成員中包含 RBBIM 子旗標，然後將 **hwndChild** 成員設定為子視窗的控制碼。 應用程式可以在 **cxMinChild** 和 **cyMinChild** 成員中設定子視窗的最小允許寬度和高度。

當 Rebar 控制項被終結時，它會終結指派給其中一個群組的任何子視窗。 若要防止控制項終結指派給其群組的子視窗，請傳送 [**rb \_ DELETEBAND**](rb-deleteband.md) 訊息來移除此群組，然後在終結 Rebar 控制項之前，先使用 [**RB \_ SETPARENT**](rb-setparent.md) 訊息將父系重設為另一個視窗。

## <a name="the-rebar-control-user-interface"></a>Rebar 控制項消費者介面

除了使用 RBBS FIXEDSIZE 樣式的所有 Rebar 控制項帶區之外，也可以調整大小 \_ 。 若要調整大小或變更控制項內的條紋順序，請按一下並拖曳一個頻外的控制條列。 Rebar 控制項會自動調整大小，並將指派給其群組的子視窗重新置放。 此外，您可以按一下寬線文字（如果有的話）來切換寬線的大小。

## <a name="the-rebar-controls-image-list"></a>Rebar 控制項的影像清單

如果應用程式使用包含 Rebar 控制項的影像清單，則必須先傳送 [**RB \_ SETBARINFO**](rb-setbarinfo.md) 訊息，然後再將區段加入控制項。 此訊息接受 [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) 結構的位址做為 *lParam* 參數。 傳送訊息之前，請將 **cbSize** 成員設定為結構的大小（以位元組為單位），以準備 **REBARINFO** 結構。 然後，如果 Rebar 控制項即將在群組上顯示影像，請將 **fMask** 成員設定為 RBIM \_ IMAGELIST 旗標，並將影像清單控制碼指派給 **himl** 成員。 如果 Rebar 不會使用頻外影像，請將 **fMask** 設定為零。

## <a name="rebar-control-message-forwarding"></a>Rebar 控制項訊息轉送

Rebar 控制項會將所有的 [**WM \_ 通知**](wm-notify.md) 視窗訊息轉寄至其父視窗。 此外，Rebar 控制項會將任何傳送給它的訊息，從指派給其群組的 windows 轉送，例如 [**wm \_ CHARTOITEM**](wm-chartoitem.md)、 [**wm \_ 命令**](/windows/desktop/menurc/wm-command)和其他訊息。

 

 