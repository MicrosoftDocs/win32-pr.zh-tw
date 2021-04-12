---
description: 用來表示畫面格分析中進度階段的列舉。
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: OFFLINEANALYSISSTAGE 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85D0288C-113A-4ABE-8EDB-ABB8F009956A
api_name:
- OFFLINEANALYSISSTAGE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf12b70acf70a654fe74b23d4bd3a196467797fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510004"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span data-ttu-id="9e7d6-103"><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE 列舉</span><span class="sxs-lookup"><span data-stu-id="9e7d6-103"><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE enumeration</span></span>

<span data-ttu-id="9e7d6-104">用來表示畫面格分析中進度階段的列舉。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-104">An enum used to indicate stages of progress in frame analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e7d6-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="9e7d6-106">常數</span><span class="sxs-lookup"><span data-stu-id="9e7d6-106">Constants</span></span>

<span data-ttu-id="9e7d6-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage \_ NotStarted**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage\_NotStarted**</span></span>  
<span data-ttu-id="9e7d6-108">畫面格分析尚未啟動。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-108">Frame analysis not yet started.</span></span>

<span data-ttu-id="9e7d6-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage\_Initializing**</span></span>  
<span data-ttu-id="9e7d6-110">) 發出 (要求初始化的畫面格分析。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-110">Frame analysis initializing (request issued).</span></span>

<span data-ttu-id="9e7d6-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage \_ 初始化 \_ LinkOk**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage\_Initializing\_LinkOk**</span></span>  
<span data-ttu-id="9e7d6-112"> (連結建立) 初始化的畫面格分析。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-112">Frame analysis initializing (link established).</span></span>

<span data-ttu-id="9e7d6-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage \_ 初始化 \_ ManifestOk**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage\_Initializing\_ManifestOk**</span></span>  
<span data-ttu-id="9e7d6-114">已成功剖析 (資訊清單) 的畫面格分析。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-114">Frame analysis initializing (manifest parsed successfully).</span></span>

<span data-ttu-id="9e7d6-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage \_ 初始化 \_ ToolOk**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage\_Initializing\_ToolOk**</span></span>  
<span data-ttu-id="9e7d6-116">初始化 (分析器載入) 的畫面格分析。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-116">Frame analysis initializing (analyzer loading).</span></span>

<span data-ttu-id="9e7d6-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage \_ 分析**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage\_Analyzing**</span></span>  
<span data-ttu-id="9e7d6-118">畫面格分析正在執行。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-118">Frame analysis is running.</span></span>

<span data-ttu-id="9e7d6-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage \_ AnalysisCompleted**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage\_AnalysisCompleted**</span></span>  
<span data-ttu-id="9e7d6-120">畫面格分析已完成 ( 傳送) 的「完成」事件。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-120">Frame analysis completed ('complete' event sent).</span></span>

<span data-ttu-id="9e7d6-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage\_AnalysisCompleted\_Successful**</span></span>  
<span data-ttu-id="9e7d6-122">畫面格分析已順利完成。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-122">Frame analysis completed successfully.</span></span>

<span data-ttu-id="9e7d6-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ OutputFileExists**</span><span class="sxs-lookup"><span data-stu-id="9e7d6-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage\_AnalysisCompleted\_OutputFileExists**</span></span>  
<span data-ttu-id="9e7d6-124">畫面格分析已完成，且輸出檔案存在。</span><span class="sxs-lookup"><span data-stu-id="9e7d6-124">Frame analysis completed and output file exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7d6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e7d6-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9e7d6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9e7d6-126">Header</span></span></p></td><td><span data-ttu-id="9e7d6-127">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9e7d6-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



