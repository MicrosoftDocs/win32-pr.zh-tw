---
title: 提供 RDP 用戶端安全性
description: 遠端桌面 ActiveX 控制項物件的某些屬性會限制為特定的 Internet Explorer URL 安全性區域。
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672991"
---
# <a name="providing-for-rdp-client-security"></a><span data-ttu-id="326ad-103">提供 RDP 用戶端安全性</span><span class="sxs-lookup"><span data-stu-id="326ad-103">Providing for RDP client security</span></span>

<span data-ttu-id="326ad-104">為了讓用戶端免于受到可能無法信任的伺服器的攻擊，遠端桌面 ActiveX 控制項物件的某些屬性會限制為特定的 Internet Explorer URL 安全性區域。</span><span class="sxs-lookup"><span data-stu-id="326ad-104">To allow clients to protect themselves from potentially untrustworthy servers, some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="326ad-105">這表示，當流覽 web 的使用者存取頁面，而且頁面的 URL 安全性區域與流覽 web 的電腦不同時，會停用這些屬性。</span><span class="sxs-lookup"><span data-stu-id="326ad-105">This means that, when a user browsing the web accesses the page and the page is in a higher URL security zone than the computer they are browsing the web with, these properties are disabled.</span></span> <span data-ttu-id="326ad-106">這些受限制的屬性可使用 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面和 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面來存取，並可在下列 Internet Explorer URL 安全性區域中取得：</span><span class="sxs-lookup"><span data-stu-id="326ad-106">These restricted properties are accessed using the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface and the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and are available in the following Internet Explorer URL security zones:</span></span>

-   <span data-ttu-id="326ad-107">我的電腦</span><span class="sxs-lookup"><span data-stu-id="326ad-107">My computer</span></span>
-   <span data-ttu-id="326ad-108">近端內部網路</span><span class="sxs-lookup"><span data-stu-id="326ad-108">Local intranet</span></span>
-   <span data-ttu-id="326ad-109">信任的網站</span><span class="sxs-lookup"><span data-stu-id="326ad-109">Trusted sites</span></span>

<span data-ttu-id="326ad-110">這些區域會在這些區域中停用：</span><span class="sxs-lookup"><span data-stu-id="326ad-110">They are disabled in these zones:</span></span>

-   <span data-ttu-id="326ad-111">網際網路</span><span class="sxs-lookup"><span data-stu-id="326ad-111">Internet</span></span>
-   <span data-ttu-id="326ad-112">限制的網站</span><span class="sxs-lookup"><span data-stu-id="326ad-112">Restricted sites</span></span>

<span data-ttu-id="326ad-113">如果您在遠端桌面服務 web 應用程式中呼叫這些受限制的屬性，您應該呼叫 [**IMsTscAx：： get \_ SecuredSettings**](imstscax-securedsettings.md) 和 [**IMsTscAx：： Get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) 來存取受保護的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="326ad-113">If you call these restricted properties within your Remote Desktop Services web application, you should call [**IMsTscAx::get\_SecuredSettings**](imstscax-securedsettings.md) and [**IMsTscAx::get\_SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) to access the Secured Settings properties.</span></span>

<span data-ttu-id="326ad-114">**IMsTscSecuredSettings** 介面所存取的受限制屬性如下：</span><span class="sxs-lookup"><span data-stu-id="326ad-114">The restricted properties that the **IMsTscSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="326ad-115">[**StartProgram**](imstscsecuredsettings-startprogram.md)。</span><span class="sxs-lookup"><span data-stu-id="326ad-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span> <span data-ttu-id="326ad-116">這個屬性會指定將在連接時啟動的程式。</span><span class="sxs-lookup"><span data-stu-id="326ad-116">This property specifies the program that will be started upon connection.</span></span>
-   <span data-ttu-id="326ad-117">[**WorkDir**](imstscsecuredsettings-workdir.md)。</span><span class="sxs-lookup"><span data-stu-id="326ad-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span></span> <span data-ttu-id="326ad-118">這個屬性會指定 [**StartProgram**](imstscsecuredsettings-startprogram.md)中指定之程式的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="326ad-118">This property specifies the working directory of the program specified in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span>
-   <span data-ttu-id="326ad-119">[**全螢幕**](imstscsecuredsettings-fullscreen.md)。</span><span class="sxs-lookup"><span data-stu-id="326ad-119">[**FullScreen**](imstscsecuredsettings-fullscreen.md).</span></span> <span data-ttu-id="326ad-120">這個屬性會指定連接時的控制項狀態是處於全螢幕模式或視窗模式。</span><span class="sxs-lookup"><span data-stu-id="326ad-120">This property specifies whether the state of the control upon connection will be in full-screen or window mode.</span></span> <span data-ttu-id="326ad-121">如果這個屬性的值為 **TRUE**，將會以全螢幕模式開啟連接。</span><span class="sxs-lookup"><span data-stu-id="326ad-121">If the value of this property is **TRUE**, the connection will be opened in full-screen mode.</span></span> <span data-ttu-id="326ad-122">雖然使用 [ **全** 螢幕] 屬性僅限於先前所列的 Internet Explorer URL 安全性區域，但是在連線之後，使用者隨時都可以按 [全螢幕模式] [快速鍵](terminal-services-shortcut-keys.md) 組合，變更為全螢幕模式 (CTRL + ALT + BREAK) 。</span><span class="sxs-lookup"><span data-stu-id="326ad-122">Although the use of the **FullScreen** property is restricted to the Internet Explorer URL security zones listed earlier, a user can always change to full-screen mode after connection by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="326ad-123">**IMsRdpClientSecuredSettings** 介面所存取的屬性如下：</span><span class="sxs-lookup"><span data-stu-id="326ad-123">The properties that the **IMsRdpClientSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="326ad-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)。</span><span class="sxs-lookup"><span data-stu-id="326ad-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span></span> <span data-ttu-id="326ad-125">這個屬性會指定是否要在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上，重新導向聲音或播放音效。</span><span class="sxs-lookup"><span data-stu-id="326ad-125">This property specifies whether to redirect sounds, or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>
-   <span data-ttu-id="326ad-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)。</span><span class="sxs-lookup"><span data-stu-id="326ad-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span></span> <span data-ttu-id="326ad-127">這個屬性會指定套用 Windows 按鍵組合的方式和時間;例如，ALT + TAB。</span><span class="sxs-lookup"><span data-stu-id="326ad-127">This property specifies how and when to apply Windows key combinations; for example, ALT+TAB.</span></span>

<span data-ttu-id="326ad-128">下列腳本會在連接時啟動 Microsoft Notepad.exe。</span><span class="sxs-lookup"><span data-stu-id="326ad-128">The following script launches Microsoft Notepad.exe upon connection.</span></span> <span data-ttu-id="326ad-129">在呼叫 [**IMsTscAx：： Connect**](imstscax-connect.md) 方法之前，請先執行此腳本。</span><span class="sxs-lookup"><span data-stu-id="326ad-129">Run this script before calling the [**IMsTscAx::Connect**](imstscax-connect.md) method.</span></span>

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




