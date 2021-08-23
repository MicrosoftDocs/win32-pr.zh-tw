---
description: .NET Framework 的安全性模型會根據應用程式來源的不同，而以不同的方式處理應用程式。
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: 安全性與信任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99806fa3256dfd08d8f4a14c70620c767331fb3cb95b83a7ecd6940b04c155cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708198"
---
# <a name="security-and-trust"></a>安全性與信任

.NET Framework 的安全性模型會根據應用程式來源的不同，而以不同的方式處理應用程式。 從使用者電腦執行的可執行檔和元件通常會以完全信任的方式執行;在網際網路上執行的相同可執行檔和元件一般都是以部分信任執行。 這是為了防止惡意程式碼讀取或修改它不應存取的資訊，例如本機檔案、剪貼簿中的專案，以及其他資源。 如果可執行檔呼叫元件，而後者又呼叫另一個需要特定層級信任的元件，則會套用鏈中所有元件的最低層級信任。 但是，電腦上的系統管理員可以設定覆寫預設許可權的特定許可權。

安全性模型的總覽是在 [安全、Light-Weight Client-Side 控制項](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer)中提供，您可以在 [實務](/previous-versions/msp-n-p/ff648663(v=pandp.10))上取得安全性模型的更深入資訊。 最好先瞭解程式庫的安全性 (這對網頁上的 [**UserControl**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) 物件特別重要，) 可以 [從部分信任的程式碼使用程式庫](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp)中找到，而在 [撰寫安全的 managed 控制項](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue)時可以找到 managed 控制項的其他安全性資訊。

## <a name="permissions"></a>權限

Tablet PC 技術 API 中大部分受管理的物件和成員都有兩個需求：

-   一律需要執行。
-   當 [InheritanceDemand](/previous-versions/windows/) 安全性動作發生時，需要 FullTrust。 這表示，當衍生類別繼承類別或從 Tablet PC SDK 覆寫方法時，就需要完全信任。

下表列出需要額外許可權的類別和成員。 指定類別的許可權也會套用到其所有未列在此資料表中的成員。



| 類別或方法                                                                       | 權限                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [System.security.permissions.uipermissionclipboard>. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**筆墨. ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [System.security.permissions.uipermissionclipboard>. OwnClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**筆墨. ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [System.security.permissions.uipermissionclipboard>. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**InkCollector**](inkcollector-class.md)                                            | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector (IntPtr)                                                                   | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/)<br/>         |
| InkCollector 控制碼                                                                   | [System.security.permissions.uipermissionwindow>. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/) (請參閱下面的附注) <br/> |
| InkEdit                                                                               | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [InkOverlay](/previous-versions/ms552322(v=vs.100))                                   | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay (IntPtr)                                                                     | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 System.security.permissions.securitypermissionflag>. UnmanagedCode<br/>                                                                 |
| [InkOverlay。控制碼](/previous-versions/ms833109(v=msdn.10))                      | [System.security.permissions.uipermissionwindow>. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/) (請參閱下面的附注) <br/> |
| [InkPicture](/previous-versions/aa514604(v=msdn.10))                                   | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| [PenInputPanel](/previous-versions/aa514041(v=msdn.10))                             | 請參閱下方注意事項。<br/>                                                                                                                                                                                     |
| [**InkRenderer**](inkrenderer-class.md)                                              | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)、 [ **DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/)<br/>         |
| 轉譯器。 InkSpaceToPixel (IntPtr、Point) 、轉譯器. InkSpaceToPixel (IntPtr、Point \[ \])     | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/)<br/>         |
| 轉譯器。 PixelToInkSpace (IntPtr、Point) 、轉譯器. PixelToInkSpace (IntPtr、Point \[ \])     | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer (IntPtr)                                                                | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**RealTimeStylus**](realtimestylus-class.md)                                        | [System.security.permissions.uipermissionwindow>. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus (IntPtr) 、RealTimeStylus (IntPtr、Boolean) 、RealTimeStylus (IntPtr、Tablet)  | [System.security.permissions.uipermissionwindow>. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) 和 [system.security.permissions.securitypermissionflag>. UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> 通常最好使用控制項來取代 (IntPtr) 的控制碼，因為控制項需要較少的許可權。 同樣地，最好是使用 Graphics 物件，而不是轉譯器的控制碼 [。 Draw](/previous-versions/ms828488(v=msdn.10))、 [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) 和 [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10))。

 

> [!Note]  
> [InkCollector](/previous-versions/ms836504(v=msdn.10))控制碼和[InkOverlay。](/previous-versions/ms833109(v=msdn.10))如果控制碼是針對 Windows Forms 控制項，則控制碼屬性不需要[system.security.permissions.securitypermissionflag> UnmanagedCode](/previous-versions/windows/)許可權，但會針對其他視窗進行。

 

> [!Note]  
> 針對 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 類別，下列方法和屬性需要 [system.security.permissions.securitypermissionflag>. AllFlags](/previous-versions/windows/)： PenInputPanel (IntPtr) 、 [AttachedEditWindow](/previous-versions/ms582240(v=vs.100))、 [忙碌](/previous-versions/ms571975(v=vs.100))、 [CommitPendingInput](/previous-versions/ms569650(v=vs.100))、 [CurrentPanel](/previous-versions/ms571976(v=vs.100))、 [DefaultPanel](/previous-versions/ms571977(v=vs.100))、 [EnableTsf](/previous-versions/ms569656(v=vs.100))、 [模擬](/previous-versions/ms571978(v=vs.100))、 [Height](/previous-versions/ms571979(v=vs.100))、 [system.windows.controls.primitives.popup.horizontaloffset](/previous-versions/ms571980(v=vs.100))、 [InputFailed](/previous-versions/ms567738(v=vs.100))、 [Left](/previous-versions/ms571981(v=vs.100))、 [MoveTo](/previous-versions/ms569667(v=vs.100))、 [PanelChanged](/previous-versions/ms567741(v=vs.100))、 [PanelMoving](/previous-versions/ms567748(v=vs.100))、 [Refresh](/previous-versions/ms569778(v=vs.100))、 [Top](/previous-versions/ms571982(v=vs.100))、 [system.windows.controls.primitives.popup.verticaloffset](/previous-versions/ms571983(v=vs.100))、 [Visible](/previous-versions/ms571984(v=vs.100))、 [VisibleChanged](/previous-versions/ms567754(v=vs.100))及 [Width](/previous-versions/ms571985(v=vs.100))。

 

## <a name="other-considerations"></a>其他考量

其他一些已知的安全性考慮如下：

-   需要 Microsoft Internet Explorer 6 或更高版本，Web 控制項才能正常運作。 使用 Internet Explorer 5.5 時，只會載入初始的 managed 控制項;您無法在執行時間動態載入其他控制項。
-   如果您使用 Windows XP Service Pack 2 (SP2) 和 clr 1.0，則在 Internet Explorer 中使用 Web 控制項，需要將網站新增為信任的網站，即使它們位於內部網路區域中也一樣。 但是，當您這樣做時，他們將無法再于信任的網站區域中執行，不過它們會在內部網路區域中執行。 這個問題是由 CLR 1.1 修正。

 

 