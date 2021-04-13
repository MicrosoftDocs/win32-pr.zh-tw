---
description: 舊版音訊應用程式的通知聲音
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: 舊版音訊應用程式的通知聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510612"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a><span data-ttu-id="fcad9-103">舊版音訊應用程式的通知聲音</span><span class="sxs-lookup"><span data-stu-id="fcad9-103">Notification Sounds for Legacy Audio Applications</span></span>

<span data-ttu-id="fcad9-104">在 Windows Vista 中，作業系統會將其所有的系統通知音效指派給跨進程音訊會話，該會話會透過目前指派給 eConsole [裝置角色](device-roles.md)的轉譯端點裝置播放。</span><span class="sxs-lookup"><span data-stu-id="fcad9-104">In Windows Vista, the operating system assigns all of its system notification sounds to a cross-process audio session that plays through the rendering endpoint device that is currently assigned to the eConsole [device role](device-roles.md).</span></span> <span data-ttu-id="fcad9-105">系統音量控制程式 Sndvol 會顯示專用於系統通知音效的音量滑杆。</span><span class="sxs-lookup"><span data-stu-id="fcad9-105">The system volume-control program, Sndvol, displays a volume slider that is dedicated to system notification sounds.</span></span>

<span data-ttu-id="fcad9-106">有些應用程式會播放通知聲音。</span><span class="sxs-lookup"><span data-stu-id="fcad9-106">Some applications play notification sounds.</span></span> <span data-ttu-id="fcad9-107">除了要求使用者透過 Sndvol 中的不同磁片區滑杆來管理應用程式的通知音效之外，應用程式也可以將其通知音效指派給與系統通知音效相同的會話。</span><span class="sxs-lookup"><span data-stu-id="fcad9-107">Instead of requiring the user to manage an application's notification sounds through a separate volume slider in Sndvol, the application can assign its notification sounds to the same session as the system notification sounds.</span></span> <span data-ttu-id="fcad9-108">控制系統通知音效的 Sndvol 音量滑杆，會控制應用程式的通知音效。</span><span class="sxs-lookup"><span data-stu-id="fcad9-108">The Sndvol volume slider that controls the system notification sounds then controls the notification sounds from the application.</span></span>

<span data-ttu-id="fcad9-109">為了啟用此行為，Windows Vista 定義了 \_ 舊版 [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 功能的 operators.snd 系統旗標。</span><span class="sxs-lookup"><span data-stu-id="fcad9-109">To enable this behavior, Windows Vista defines a SND\_SYSTEM flag for the legacy [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function.</span></span> <span data-ttu-id="fcad9-110"> (舊版 Windows 中不支援此旗標，包括 Windows Server 2003、Windows XP 及 Windows 2000 ) 。如果呼叫端設定此旗標，則 **PlaySound** 函式會將它所播放的音效指派給作業系統用於其通知音效的跨進程會話。</span><span class="sxs-lookup"><span data-stu-id="fcad9-110">(This flag is not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.) If the caller sets this flag, then the **PlaySound** function assigns the sound that it plays to the cross-process session that the operating system uses for its notification sounds.</span></span> <span data-ttu-id="fcad9-111">如果呼叫端未設定旗標，則 **PlaySound** 會將它所播放的音效指派給預設會話，也就是由會話 GUID 值 guid Null 所識別的進程特定會話 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fcad9-111">If the caller does not set the flag, then **PlaySound** assigns the sound that it plays to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span> <span data-ttu-id="fcad9-112">OPERATORS.SND \_ 系統定義于標頭檔 Mmsystem 中。</span><span class="sxs-lookup"><span data-stu-id="fcad9-112">SND\_SYSTEM is defined in the header file Mmsystem.h.</span></span> <span data-ttu-id="fcad9-113">如需 **PlaySound** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="fcad9-113">For more information about **PlaySound**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcad9-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="fcad9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcad9-115">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="fcad9-115">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
