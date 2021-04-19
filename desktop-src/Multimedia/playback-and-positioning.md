---
title: 播放和定位
description: 播放和定位
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968838"
---
# <a name="playback-and-positioning"></a><span data-ttu-id="610cf-103">播放和定位</span><span class="sxs-lookup"><span data-stu-id="610cf-103">Playback and Positioning</span></span>

<span data-ttu-id="610cf-104">多個 MCI 命令，例如 [**play**](play.md) ([**mci \_ play**](mci-play.md)) 、 [**停止**](stop.md) ([**mci \_ 停止**](mci-stop.md)) 、 [**暫停**](pause.md) ([**mci \_ 暫停**](mci-pause.md)) 、 [**繼續**](resume.md) ([**mci 搜尋) \_**](mci-resume.md) ，以及 [**搜尋**](seek.md) (mci [**\_ 搜尋**](mci-seek.md)) ，以影響多媒體檔案的播放或定位。</span><span class="sxs-lookup"><span data-stu-id="610cf-104">A number of MCI commands, such as [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)), and [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)), affect the playback or positioning of a multimedia file.</span></span> <span data-ttu-id="610cf-105">如果 MCI 裝置在另一個播放命令正在進行時收到播放命令，它會接受命令，並停止或取代上一個命令。</span><span class="sxs-lookup"><span data-stu-id="610cf-105">If an MCI device receives a playback command while another playback command is in progress, it accepts the command and either stops or supersedes the previous command.</span></span>

<span data-ttu-id="610cf-106">許多 MCI 命令（例如 [**set**](set.md) ([**mci \_ set**](mci-set.md)) ）不會影響播放。</span><span class="sxs-lookup"><span data-stu-id="610cf-106">Many MCI commands, such as [**set**](set.md) ([**MCI\_SET**](mci-set.md)), do not affect playback.</span></span> <span data-ttu-id="610cf-107">只要沒有從驅動程式的相同實例執行通知，來自其中一個命令的通知就不會干擾暫止的播放或定位命令。</span><span class="sxs-lookup"><span data-stu-id="610cf-107">A notification from one of these commands does not interfere with pending playback or position commands as long as the notifications are not performed from the same instance of the driver.</span></span> <span data-ttu-id="610cf-108">例如，您可以在裝置執行 **搜尋** 命令而不停止或取代 **搜尋** 命令的情況下， ([**MCI \_ 狀態**](mci-status.md)) 命令發出 **設定** 或 [**狀態**](status.md)。</span><span class="sxs-lookup"><span data-stu-id="610cf-108">For example, you can issue a **set** or [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command while a device is performing a **seek** command without stopping or superseding the **seek** command.</span></span>

<span data-ttu-id="610cf-109">不過，只能有一個暫止的通知。</span><span class="sxs-lookup"><span data-stu-id="610cf-109">However, there can be only one pending notification.</span></span> <span data-ttu-id="610cf-110">例如，如果應用程式要求 **播放** 通知，並遵循「開始位置通知」 **狀態** 的要求，則 **播放** 通知會傳回「已取代」，而「狀態」命令的通知會在完成時傳回。</span><span class="sxs-lookup"><span data-stu-id="610cf-110">For example, if an application requests a notification for **play** and follows that request with **status** "start position notify," the **play** notification will return "superseded" and the notification for the status command will return when it is finished.</span></span> <span data-ttu-id="610cf-111">不過，在此情況下，即使應用程式未收到通知， **播放** 命令仍會成功。</span><span class="sxs-lookup"><span data-stu-id="610cf-111">In this case, however, the **play** command will still succeed, even though the application did not receive the notification.</span></span>

 

 




