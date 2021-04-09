---
description: 代表實驗觸發程式資訊。
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ExperimentTrigger 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846212"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span data-ttu-id="21033-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger 結構</span><span class="sxs-lookup"><span data-stu-id="21033-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger structure</span></span>

<span data-ttu-id="21033-104">代表實驗觸發程式資訊。</span><span class="sxs-lookup"><span data-stu-id="21033-104">Represents experiment trigger information.</span></span>

## <a name="syntax"></a><span data-ttu-id="21033-105">語法</span><span class="sxs-lookup"><span data-stu-id="21033-105">Syntax</span></span>


```C++
} ExperimentTrigger;
```

## <a name="members"></a><span data-ttu-id="21033-106">成員</span><span class="sxs-lookup"><span data-stu-id="21033-106">Members</span></span>

<span data-ttu-id="21033-107">**type**</span><span class="sxs-lookup"><span data-stu-id="21033-107">**type**</span></span>  
<span data-ttu-id="21033-108">觸發 (capture) 的實驗類型。</span><span class="sxs-lookup"><span data-stu-id="21033-108">The kind of experiment (capture) triggered.</span></span>

<span data-ttu-id="21033-109">**key**</span><span class="sxs-lookup"><span data-stu-id="21033-109">**key**</span></span>  
<span data-ttu-id="21033-110">當 type 等於 EXPERIMENTTRIGGERTYPE：： KEY 時，用來觸發 capture 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="21033-110">When type is equal to EXPERIMENTTRIGGERTYPE::KEY, the key used to trigger capture.</span></span>

<span data-ttu-id="21033-111">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="21033-111">**frameNumber**</span></span>  
<span data-ttu-id="21033-112">當 type 等於 EXPERIMENTTRIGGERTYPE：： FRAMENUMBER 時，將會觸發 capture 的框架編號。</span><span class="sxs-lookup"><span data-stu-id="21033-112">When type is equal to EXPERIMENTTRIGGERTYPE::FRAMENUMBER, the frame number that will trigger capture.</span></span>

<span data-ttu-id="21033-113">**captureCount**</span><span class="sxs-lookup"><span data-stu-id="21033-113">**captureCount**</span></span>  
<span data-ttu-id="21033-114">要捕捉的連續框架數目。</span><span class="sxs-lookup"><span data-stu-id="21033-114">The number of sequential frames to capture.</span></span>

<span data-ttu-id="21033-115">**actionIID**</span><span class="sxs-lookup"><span data-stu-id="21033-115">**actionIID**</span></span>  
<span data-ttu-id="21033-116">動作事件的識別碼 (螢幕擷取畫面、框架捕獲等) 。</span><span class="sxs-lookup"><span data-stu-id="21033-116">The ID of the action event (screenshot, frame capture, etc).</span></span>

<span data-ttu-id="21033-117">**actionPlayload**</span><span class="sxs-lookup"><span data-stu-id="21033-117">**actionPlayload**</span></span>  
<span data-ttu-id="21033-118">動作事件裝載的指標。</span><span class="sxs-lookup"><span data-stu-id="21033-118">A pointer to the action event payload.</span></span>

## <a name="requirements"></a><span data-ttu-id="21033-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="21033-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="21033-120">標頭</span><span class="sxs-lookup"><span data-stu-id="21033-120">Header</span></span></p></td><td><span data-ttu-id="21033-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="21033-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



