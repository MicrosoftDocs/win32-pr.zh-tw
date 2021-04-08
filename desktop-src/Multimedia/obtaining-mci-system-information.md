---
title: 取得 MCI 系統資訊
description: 取得 MCI 系統資訊
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932116"
---
# <a name="obtaining-mci-system-information"></a><span data-ttu-id="cfadd-104">取得 MCI 系統資訊</span><span class="sxs-lookup"><span data-stu-id="cfadd-104">Obtaining MCI System Information</span></span>

<span data-ttu-id="cfadd-105">[Sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) 命令會取得有關 MCI 裝置的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="cfadd-105">The [sysinfo](sysinfo.md) ([**MCI\_SYSINFO**](mci-sysinfo.md)) command obtains system information about MCI devices.</span></span> <span data-ttu-id="cfadd-106">MCI 會處理此命令，而不將它轉送到任何 MCI 裝置。</span><span class="sxs-lookup"><span data-stu-id="cfadd-106">MCI handles this command without relaying it to any MCI device.</span></span> <span data-ttu-id="cfadd-107">針對命令訊息介面，MCI 會傳回 [**mci \_ SYSINFO \_ PARMS**](mci-sysinfo-parms.md) 結構中的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="cfadd-107">For the command-message interface, MCI returns the system information in the [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

<span data-ttu-id="cfadd-108">您可以使用 **sysinfo** (MCI \_ sysinfo) 命令來取得資訊，例如系統上的 mci 裝置數目、特定類型的 mci 裝置數目、開啟的 MCI 裝置數目，以及裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfadd-108">You can use the **sysinfo** (MCI\_SYSINFO) command to retrieve information such as the number of MCI devices on a system, the number of MCI devices of a particular type, the number of open MCI devices, and the names of the devices.</span></span> <span data-ttu-id="cfadd-109">此命令通常會被呼叫一次以上，以抓取特定的資訊片段。</span><span class="sxs-lookup"><span data-stu-id="cfadd-109">This command is often called more than once to retrieve a particular piece of information.</span></span> <span data-ttu-id="cfadd-110">例如，您可能會在第一次呼叫中取得特定類型的裝置數目，然後在下一步列舉裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfadd-110">For example, you might retrieve the number of devices of a particular type in the first call and then enumerate the names of the devices in the next.</span></span>

 

 




