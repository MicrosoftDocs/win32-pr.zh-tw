---
description: 您可以使用 Logman 工具，針對使用自動化系統復原 (ASR) 的 VSS 應用程式收集追蹤資訊。
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: 使用追蹤工具搭配 ASR 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971000"
---
# <a name="using-tracing-tools-with-asr-applications"></a><span data-ttu-id="0bc36-103">使用追蹤工具搭配 ASR 應用程式</span><span class="sxs-lookup"><span data-stu-id="0bc36-103">Using Tracing Tools with ASR Applications</span></span>

<span data-ttu-id="0bc36-104">您可以使用 Logman 工具，針對使用 [自動化系統復原 (ASR) ](using-vss-automated-system-recovery-for-disaster-recovery.md)的 VSS 應用程式收集追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="0bc36-104">You can use the Logman tool to collect tracing information for VSS applications that use [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span> <span data-ttu-id="0bc36-105">Logman (logman.exe) 是追蹤事件和效能計數器的追蹤控制器。</span><span class="sxs-lookup"><span data-stu-id="0bc36-105">Logman (logman.exe) is a trace controller for trace events and performance counters.</span></span> <span data-ttu-id="0bc36-106">它包含在 Windows XP 和更新版本的 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="0bc36-106">It is included in Windows XP and later versions of Windows.</span></span> <span data-ttu-id="0bc36-107">或者，如果您想要的話，也可以使用 Tracelog.exe 工具來收集相同的 ASR 追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="0bc36-107">Or, if you prefer, you can use the Tracelog tool to collect the same ASR tracing information.</span></span> <span data-ttu-id="0bc36-108">Tracelog.exe 包含在 Windows 驅動程式套件 (WDK) 中。</span><span class="sxs-lookup"><span data-stu-id="0bc36-108">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="0bc36-109">若要搭配使用追蹤工具與 VSS，請參閱搭配 [Vss 使用追蹤工具](using-tracing-tools-with-vss.md)。</span><span class="sxs-lookup"><span data-stu-id="0bc36-109">To use tracing tools with VSS, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="using-logman"></a><span data-ttu-id="0bc36-110">使用 Logman</span><span class="sxs-lookup"><span data-stu-id="0bc36-110">Using Logman</span></span>

<span data-ttu-id="0bc36-111">下列程式說明如何搭配使用 Logman 與 ASR 應用程式。</span><span class="sxs-lookup"><span data-stu-id="0bc36-111">The following procedure describes how to use Logman with your ASR application.</span></span>

<span data-ttu-id="0bc36-112">**使用 Logman 搭配您的 ASR 應用程式**</span><span class="sxs-lookup"><span data-stu-id="0bc36-112">**To use Logman with your ASR application**</span></span>

1.  <span data-ttu-id="0bc36-113">使用下列命令來開始追蹤：</span><span class="sxs-lookup"><span data-stu-id="0bc36-113">Use the following command to start tracing:</span></span>

    <span data-ttu-id="0bc36-114">**logman 啟動 asr-o** *x： \\ \* \* \* asr-ets-p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span><span class="sxs-lookup"><span data-stu-id="0bc36-114">**logman start asr -o** *x:\\*\*\*asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="0bc36-115">以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。</span><span class="sxs-lookup"><span data-stu-id="0bc36-115">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="0bc36-116">為了達到最佳效能，追蹤記錄檔應該位於不是陰影複製一部分的磁片區上。</span><span class="sxs-lookup"><span data-stu-id="0bc36-116">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

2.  <span data-ttu-id="0bc36-117">使用下列命令停止追蹤：</span><span class="sxs-lookup"><span data-stu-id="0bc36-117">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="0bc36-118">**logman 停止 asr-ets**</span><span class="sxs-lookup"><span data-stu-id="0bc36-118">**logman stop asr -ets**</span></span>

<span data-ttu-id="0bc36-119">追蹤記錄檔為 *x： \\* asr。</span><span class="sxs-lookup"><span data-stu-id="0bc36-119">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="0bc36-120">如需 Logman 工具的詳細資訊，請參閱 [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="0bc36-120">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="0bc36-121">使用 Tracelog.exe</span><span class="sxs-lookup"><span data-stu-id="0bc36-121">Using Tracelog</span></span>

<span data-ttu-id="0bc36-122">下列程式說明如何使用 Tracelog.exe。</span><span class="sxs-lookup"><span data-stu-id="0bc36-122">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="0bc36-123">**使用 Tracelog.exe**</span><span class="sxs-lookup"><span data-stu-id="0bc36-123">**To use Tracelog**</span></span>

1.  <span data-ttu-id="0bc36-124">建立名為 asr 的文字檔，其中只包含下列文字：</span><span class="sxs-lookup"><span data-stu-id="0bc36-124">Create a text file named asr.ctl that contains only the following text:</span></span>

    <span data-ttu-id="0bc36-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span><span class="sxs-lookup"><span data-stu-id="0bc36-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span></span>

2.  <span data-ttu-id="0bc36-126">使用下列命令來開始追蹤：</span><span class="sxs-lookup"><span data-stu-id="0bc36-126">Use the following command to start tracing:</span></span>

    <span data-ttu-id="0bc36-127">**tracelog.exe-啟動 asr-f** *x： \\ \* \* \* asr-guid asr。 ctl-旗標 0xff-level 0xff*\*</span><span class="sxs-lookup"><span data-stu-id="0bc36-127">**tracelog -start asr -f** *x:\\*\*\*asr.etl -guid asr.ctl -flag 0xff -level 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="0bc36-128">以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。</span><span class="sxs-lookup"><span data-stu-id="0bc36-128">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="0bc36-129">為了達到最佳效能，追蹤記錄檔應該位於不是陰影複製一部分的磁片區上。</span><span class="sxs-lookup"><span data-stu-id="0bc36-129">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

3.  <span data-ttu-id="0bc36-130">使用下列命令停止追蹤：</span><span class="sxs-lookup"><span data-stu-id="0bc36-130">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="0bc36-131">**tracelog.exe-停止 asr**</span><span class="sxs-lookup"><span data-stu-id="0bc36-131">**tracelog -stop asr**</span></span>

<span data-ttu-id="0bc36-132">追蹤記錄檔為 *x： \\* asr。</span><span class="sxs-lookup"><span data-stu-id="0bc36-132">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="0bc36-133">如需 Tracelog.exe 工具的詳細資訊，請參閱 [tracelog.exe](https://msdn.microsoft.com/library/ms797927.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0bc36-133">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
