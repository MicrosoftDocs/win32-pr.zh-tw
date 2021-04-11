---
description: 表示管線階段，包括所使用之著色器的詳細資料。
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PipeLineStage 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935783"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span data-ttu-id="3e35c-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage 結構</span><span class="sxs-lookup"><span data-stu-id="3e35c-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage structure</span></span>

<span data-ttu-id="3e35c-104">表示管線階段，包括所使用之著色器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3e35c-104">Represents a pipeline stage, including details of the shader used.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e35c-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e35c-105">Syntax</span></span>


```C++
} PipeLineStage;
```

## <a name="members"></a><span data-ttu-id="3e35c-106">成員</span><span class="sxs-lookup"><span data-stu-id="3e35c-106">Members</span></span>

<span data-ttu-id="3e35c-107">**StageId**</span><span class="sxs-lookup"><span data-stu-id="3e35c-107">**StageId**</span></span>  
<span data-ttu-id="3e35c-108">管線階段的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e35c-108">The ID of the pipeline stage.</span></span>

<span data-ttu-id="3e35c-109">**可偵錯**</span><span class="sxs-lookup"><span data-stu-id="3e35c-109">**Debuggable**</span></span>  
<span data-ttu-id="3e35c-110">如果管線階段支援調試，則為 true。否則為 false。</span><span class="sxs-lookup"><span data-stu-id="3e35c-110">true if the pipeline stage supports debugging; otherwise, false.</span></span>

<span data-ttu-id="3e35c-111">**StageName**</span><span class="sxs-lookup"><span data-stu-id="3e35c-111">**StageName**</span></span>  
<span data-ttu-id="3e35c-112">包含管線階段名稱的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="3e35c-112">A COM string containing the name of the pipeline stage.</span></span>

<span data-ttu-id="3e35c-113">**GuaranteedOutput**</span><span class="sxs-lookup"><span data-stu-id="3e35c-113">**GuaranteedOutput**</span></span>  
<span data-ttu-id="3e35c-114">如果管線階段一律具有管線輸出，則為 true。否則為 false。</span><span class="sxs-lookup"><span data-stu-id="3e35c-114">true if the pipeline stage always has pipeline output; otherwise, false.</span></span>

<span data-ttu-id="3e35c-115">**DebugEntryPoint**</span><span class="sxs-lookup"><span data-stu-id="3e35c-115">**DebugEntryPoint**</span></span>  
<span data-ttu-id="3e35c-116">包含著色器進入點名稱的 COM 字串（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3e35c-116">A COM string containing the name of the shader entry point, if there is one.</span></span>

<span data-ttu-id="3e35c-117">**ShaderFile**</span><span class="sxs-lookup"><span data-stu-id="3e35c-117">**ShaderFile**</span></span>  
<span data-ttu-id="3e35c-118">COM 字串，其中包含著色器原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="3e35c-118">A COM string containing the filepath of the shader source file.</span></span>

<span data-ttu-id="3e35c-119">**ShaderByteStreamPtr**</span><span class="sxs-lookup"><span data-stu-id="3e35c-119">**ShaderByteStreamPtr**</span></span>  
<span data-ttu-id="3e35c-120">著色器位元組資料流程的 FILEPTR。</span><span class="sxs-lookup"><span data-stu-id="3e35c-120">A FILEPTR for the shader byte stream.</span></span> <span data-ttu-id="3e35c-121">這會傳回，以便進行 debug。</span><span class="sxs-lookup"><span data-stu-id="3e35c-121">This is passed back in order to debug.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e35c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e35c-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3e35c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3e35c-123">Header</span></span></p></td><td><span data-ttu-id="3e35c-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="3e35c-124">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



