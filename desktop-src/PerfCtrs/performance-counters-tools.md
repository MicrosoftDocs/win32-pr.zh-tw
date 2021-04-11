---
description: 下表列出
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: 效能計數器工具
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944244"
---
# <a name="performance-counters-tools"></a><span data-ttu-id="e8e74-103">效能計數器工具</span><span class="sxs-lookup"><span data-stu-id="e8e74-103">Performance Counters Tools</span></span>

## <a name="data-collection-tools"></a><span data-ttu-id="e8e74-104">資料收集工具</span><span class="sxs-lookup"><span data-stu-id="e8e74-104">Data collection tools</span></span>

<span data-ttu-id="e8e74-105">使用或操作 Windows 效能計數器資料時，下列工具很有用。</span><span class="sxs-lookup"><span data-stu-id="e8e74-105">The following tools are useful when consuming or manipulating Windows Performance Counter data.</span></span>

|<span data-ttu-id="e8e74-106">工具</span><span class="sxs-lookup"><span data-stu-id="e8e74-106">Tool</span></span>|<span data-ttu-id="e8e74-107">描述</span><span class="sxs-lookup"><span data-stu-id="e8e74-107">Description</span></span>
|----|-----------
| [<span data-ttu-id="e8e74-108">PerfMon</span><span class="sxs-lookup"><span data-stu-id="e8e74-108">PerfMon</span></span>](/windows-server/administration/windows-commands/perfmon) | <span data-ttu-id="e8e74-109">用來收集和查看效能計數器資料的 GUI 工具。</span><span class="sxs-lookup"><span data-stu-id="e8e74-109">GUI tool for collecting and viewing Performance Counter data.</span></span> <span data-ttu-id="e8e74-110">`perfmon.exe` 使用效能監視器嵌入式管理單元啟動 MMC，以提供效能監視器、資料收集器集合工具和報表工具的存取權。</span><span class="sxs-lookup"><span data-stu-id="e8e74-110">`perfmon.exe` launches MMC with the Performance Monitor snap-in, which provides access to the Performance Monitor, Data Collector Sets, and Reports tools.</span></span>
| [<span data-ttu-id="e8e74-111">TypePerf</span><span class="sxs-lookup"><span data-stu-id="e8e74-111">TypePerf</span></span>](/windows-server/administration/windows-commands/typeperf) |<span data-ttu-id="e8e74-112">用來收集和列印效能計數器資料的命令列工具。</span><span class="sxs-lookup"><span data-stu-id="e8e74-112">Command-line tool for collecting and printing Performance Counter data.</span></span> <span data-ttu-id="e8e74-113">可以用來列出可用的 countersets、列出可用的計數器、將計數器資料列印到主控台，或將計數器資料收集到記錄檔 (CSV、.TDF、.BLG) 。</span><span class="sxs-lookup"><span data-stu-id="e8e74-113">Can be used to list available countersets, list available counters, print counter data to the console, or collect counter data to a log file (CSV, TDF, BLG).</span></span>
| [<span data-ttu-id="e8e74-114">重新記錄</span><span class="sxs-lookup"><span data-stu-id="e8e74-114">Relog</span></span>](/windows-server/administration/windows-commands/relog) |<span data-ttu-id="e8e74-115">命令列工具，可用於轉換和合併記錄檔 (CSV、.TDF、.BLG) 透過 `typeperf.exe` 或透過 api 來捕捉 `PDH.dll` 。</span><span class="sxs-lookup"><span data-stu-id="e8e74-115">Command-line tool for transforming and merging log files (CSV, TDF, BLG) captured via `typeperf.exe` or via the `PDH.dll` APIs.</span></span>
| [<span data-ttu-id="e8e74-116">LogMan</span><span class="sxs-lookup"><span data-stu-id="e8e74-116">LogMan</span></span>](/windows-server/administration/windows-commands/logman) |<span data-ttu-id="e8e74-117">用來控制資料收集器集合工具的命令列工具。</span><span class="sxs-lookup"><span data-stu-id="e8e74-117">Command-line tool for controlling Data Collector Sets.</span></span>

## <a name="data-provider-tools"></a><span data-ttu-id="e8e74-118">資料提供者工具</span><span class="sxs-lookup"><span data-stu-id="e8e74-118">Data provider tools</span></span>

<span data-ttu-id="e8e74-119">下列工具適用于發佈 Windows 效能計數器資料時。</span><span class="sxs-lookup"><span data-stu-id="e8e74-119">The following tools are useful when publishing Windows Performance Counter data.</span></span>

|<span data-ttu-id="e8e74-120">工具</span><span class="sxs-lookup"><span data-stu-id="e8e74-120">Tool</span></span>|<span data-ttu-id="e8e74-121">描述</span><span class="sxs-lookup"><span data-stu-id="e8e74-121">Description</span></span>
|----|-----------
| [<span data-ttu-id="e8e74-122">CtrPP</span><span class="sxs-lookup"><span data-stu-id="e8e74-122">CtrPP</span></span>](ctrpp.md) | <span data-ttu-id="e8e74-123">Windows SDK 中的命令列組建工具，可驗證及編譯您的效能計數器 V2 提供者資訊清單。</span><span class="sxs-lookup"><span data-stu-id="e8e74-123">Command-line build tool from the Windows SDK that validates and compiles your Performance Counters V2 provider manifest.</span></span> <span data-ttu-id="e8e74-124">此工具會產生 `.h` `.rc` 建立 V2 提供者所需的標頭和資源腳本。</span><span class="sxs-lookup"><span data-stu-id="e8e74-124">This tool generates the `.h` headers and `.rc` resource scripts needed to build a V2 provider.</span></span>
| [<span data-ttu-id="e8e74-125">LodCtr</span><span class="sxs-lookup"><span data-stu-id="e8e74-125">LodCtr</span></span>](/windows-server/administration/windows-commands/lodctr) | <span data-ttu-id="e8e74-126">命令列工具，用來將提供者安裝到系統上。</span><span class="sxs-lookup"><span data-stu-id="e8e74-126">Command-line tool used to install your provider onto a system.</span></span>
| [<span data-ttu-id="e8e74-127">UnlodCtr</span><span class="sxs-lookup"><span data-stu-id="e8e74-127">UnlodCtr</span></span>](/windows-server/administration/windows-commands/unlodctr_1) | <span data-ttu-id="e8e74-128">命令列工具，用來從系統卸載您的提供者。</span><span class="sxs-lookup"><span data-stu-id="e8e74-128">Command-line tool used to uninstall your provider from a system.</span></span>
