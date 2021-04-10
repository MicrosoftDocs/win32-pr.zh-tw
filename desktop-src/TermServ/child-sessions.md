---
title: 子會話
description: 從 Windows Server 2012 和 Windows 8 開始，遠端桌面支援子會話的概念，也就是系結至使用者現有會話的特殊回送遠端桌面會話。
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183041"
---
# <a name="child-sessions"></a><span data-ttu-id="45a77-103">子會話</span><span class="sxs-lookup"><span data-stu-id="45a77-103">Child Sessions</span></span>

<span data-ttu-id="45a77-104">從 Windows Server 2012 和 Windows 8 開始，遠端桌面支援 *子會話* 的概念，也就是系結至使用者現有會話的特殊回送遠端桌面會話。</span><span class="sxs-lookup"><span data-stu-id="45a77-104">Beginning with Windows Server 2012 and Windows 8, Remote Desktop supports the concept of a *child session*, which is a special loopback Remote Desktop session that is tied to a user's existing session.</span></span>

<span data-ttu-id="45a77-105">下列作業系統不支援子會話：</span><span class="sxs-lookup"><span data-stu-id="45a77-105">Child sessions are not supported on the following operating systems:</span></span>

<dl> <span data-ttu-id="45a77-106">Windows RT</span><span class="sxs-lookup"><span data-stu-id="45a77-106">Windows RT</span></span>  
<span data-ttu-id="45a77-107">Windows Server 2012 Server Core 安裝選項</span><span class="sxs-lookup"><span data-stu-id="45a77-107">Windows Server 2012 Server Core installation option</span></span>  
<span data-ttu-id="45a77-108">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="45a77-108">Microsoft Hyper-V Server 2012</span></span>  
</dl>

<span data-ttu-id="45a77-109">在任何指定時間，系統一次只能有一個作用中且已連線的子會話。</span><span class="sxs-lookup"><span data-stu-id="45a77-109">A system can only have one active and connected child session at any given time.</span></span>

<span data-ttu-id="45a77-110">您可以直接登出子會話，或在父會話終止時將其終止。</span><span class="sxs-lookup"><span data-stu-id="45a77-110">The child session can be terminated by logging off directly from it, or it will be terminated when its parent session terminates.</span></span>

<span data-ttu-id="45a77-111">您必須藉由呼叫 [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) 函式來啟用子會話功能，才可以在系統上使用子會話。</span><span class="sxs-lookup"><span data-stu-id="45a77-111">Before child sessions can be used on a system, you must enable the child session functionality by calling the [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) function.</span></span> <span data-ttu-id="45a77-112">您也可以使用 [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) 函式來判斷子會話是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="45a77-112">You can also determine if child sessions have been enabled by using the [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) function.</span></span>

<span data-ttu-id="45a77-113">使用 [遠端桌面 ActiveX 控制項](remote-desktop-activex-control.md) ，然後在連接之前設定 "ConnectToChildSession" 屬性與 [**IMsRdpExtendedSettings**](imsrdpextendedsettings-property.md) ，就可以從現有使用者的會話內建立子會話。</span><span class="sxs-lookup"><span data-stu-id="45a77-113">A child session can only be created from within an existing user's session by using the [Remote Desktop ActiveX control](remote-desktop-activex-control.md) and setting the "ConnectToChildSession" property with [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prior to connecting.</span></span> <span data-ttu-id="45a77-114">呼叫 [**IMsTscAx**](imstscax-connect.md) 方法時，除非使用者使用智慧卡登入父會話，否則遠端桌面 ActiveX 控制項會自動登入子會話，而不會提示輸入認證。</span><span class="sxs-lookup"><span data-stu-id="45a77-114">When the [**IMsTscAx.Connect**](imstscax-connect.md) method is called, the Remote Desktop ActiveX control will automatically log on to the child session without prompting for credentials, except when the user is logged into the parent session using a smart card.</span></span> <span data-ttu-id="45a77-115">不同于一般的遠端桌面會話，使用者不需要遠端互動式許可權即可登入子會話，因為這是回送會話。</span><span class="sxs-lookup"><span data-stu-id="45a77-115">Unlike a regular Remote Desktop session, a user does not need the Remote Interactive right to log on to the child session because this is a loopback session.</span></span>

<span data-ttu-id="45a77-116">子會話無法鎖定。</span><span class="sxs-lookup"><span data-stu-id="45a77-116">A child session cannot be locked.</span></span> <span data-ttu-id="45a77-117">它不會有螢幕保護裝置和登入畫面。</span><span class="sxs-lookup"><span data-stu-id="45a77-117">It will have no screen saver and no logon screen.</span></span> <span data-ttu-id="45a77-118">此外，與一般會話不同的是，如果設定 WinLogon 登入文字原則，登入文字將不會顯示在此子會話中。</span><span class="sxs-lookup"><span data-stu-id="45a77-118">Also, unlike a regular session, if the WinLogon logon text policy is set, the logon text will not be displayed in this child session.</span></span> <span data-ttu-id="45a77-119">此外，如果已設定這些原則，子會話的遠端桌面連線 Timeout 群組原則就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="45a77-119">Also, there will be no effect of Remote Desktop Connection Timeout Group policies on the child session if these policies are set.</span></span>

<span data-ttu-id="45a77-120">下列 Api 會與子會話搭配使用：</span><span class="sxs-lookup"><span data-stu-id="45a77-120">The following APIs are used in conjunction with child sessions:</span></span>

-   [<span data-ttu-id="45a77-121">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="45a77-121">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [<span data-ttu-id="45a77-122">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="45a77-122">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [<span data-ttu-id="45a77-123">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="45a77-123">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   <span data-ttu-id="45a77-124">IMsRdpExtendedSettings 中的 "ConnectToChildSession" 屬性 [ **。屬性**](imsrdpextendedsettings-property.md)</span><span class="sxs-lookup"><span data-stu-id="45a77-124">"ConnectToChildSession" property in [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)</span></span>

 

 




