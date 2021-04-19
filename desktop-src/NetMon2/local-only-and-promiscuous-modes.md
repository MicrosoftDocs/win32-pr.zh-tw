---
description: 監視器可以在僅限原生模式或混合模式中檢查畫面格。
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only 和混合模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973866"
---
# <a name="local-only-and-promiscuous-modes"></a><span data-ttu-id="6ce8e-103">Local-Only 和混合模式</span><span class="sxs-lookup"><span data-stu-id="6ce8e-103">Local-Only and Promiscuous Modes</span></span>

<span data-ttu-id="6ce8e-104">監視器可以在僅限原生模式或混合模式中檢查畫面格。</span><span class="sxs-lookup"><span data-stu-id="6ce8e-104">Monitors can examine frames in local-only mode or promiscuous mode.</span></span>

<span data-ttu-id="6ce8e-105">在僅限原生模式中， (NPP) 的網路封包提供者會傳回執行監視的電腦所傳送的框架，包括導向至本機電腦的廣播和多播。</span><span class="sxs-lookup"><span data-stu-id="6ce8e-105">In local-only mode, the network packet provider (NPP) returns frames that are sent to or from the computer on which the monitor is running, including broadcasts and multicasts directed to the local machine.</span></span> <span data-ttu-id="6ce8e-106">雖然受限於本機導向的框架，但原生模式也會比處理器密集。</span><span class="sxs-lookup"><span data-stu-id="6ce8e-106">Although limited to locally directed frames, local-mode is also much less processor intensive.</span></span>

<span data-ttu-id="6ce8e-107">在混合模式中，監視器也可以監看沒有導向至本機電腦或從本機電腦導向的流量。</span><span class="sxs-lookup"><span data-stu-id="6ce8e-107">In promiscuous mode, the monitor can also watch for traffic that is not directed to or from the local computer.</span></span> <span data-ttu-id="6ce8e-108">除非監視器已指定旗標 [ \_ 不需要 MCS 建立 PMODE]，否則在 OnLoadingDLL 函式 \_ \_ \_ 中，監視器控制服務 (MCSVC) 會假設監視器在載入監視器 DLL 時需要混合模式。 [](onloadingdll.md)</span><span class="sxs-lookup"><span data-stu-id="6ce8e-108">Unless the monitor has specified the flag, MCS\_CREATE\_PMODE\_NOT\_REQUIRED, in the [OnLoadingDLL](onloadingdll.md) function, the Monitor Control Service (MCSVC) assumes that the monitor requires promiscuous mode when it loads the monitor DLL.</span></span>

 

 



