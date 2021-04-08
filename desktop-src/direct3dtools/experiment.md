---
description: 表示實驗 (capture) 的相關資訊。
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 實驗結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687899"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span data-ttu-id="6d5a0-103"><span id="vspixengine.experiment"></span>實驗結構</span><span class="sxs-lookup"><span data-stu-id="6d5a0-103"><span id="vspixengine.experiment"></span>Experiment structure</span></span>

<span data-ttu-id="6d5a0-104">表示實驗 (capture) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-104">Represents information about an experiment (capture).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="6d5a0-105">Syntax</span></span>


```C++
} Experiment;
```

## <a name="members"></a><span data-ttu-id="6d5a0-106">成員</span><span class="sxs-lookup"><span data-stu-id="6d5a0-106">Members</span></span>

<span data-ttu-id="6d5a0-107">**進程**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-107">**processId**</span></span>  
<span data-ttu-id="6d5a0-108">相關聯的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-108">The associated process ID.</span></span>

<span data-ttu-id="6d5a0-109">**applicationName**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-109">**applicationName**</span></span>  
<span data-ttu-id="6d5a0-110">COM 字串，其中包含要執行實驗的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-110">A COM string containing the name of the application to run the experiment on.</span></span>

<span data-ttu-id="6d5a0-111">**commandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-111">**commandLineArguments**</span></span>  
<span data-ttu-id="6d5a0-112">包含命令列引數的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-112">A COM string containing the command line arguments.</span></span>

<span data-ttu-id="6d5a0-113">**workingDirectory**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-113">**workingDirectory**</span></span>  
<span data-ttu-id="6d5a0-114">包含工作目錄路徑的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-114">A COM string containing the path of the working directory.</span></span>

<span data-ttu-id="6d5a0-115">**tempPixRunFile**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-115">**tempPixRunFile**</span></span>  
<span data-ttu-id="6d5a0-116">COM 字串，其中包含用來執行實驗之暫存檔案的 filepath。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-116">A COM string containing the filepath of the temporary file used to perform the experiment.</span></span>

<span data-ttu-id="6d5a0-117">**startOption**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-117">**startOption**</span></span>  
<span data-ttu-id="6d5a0-118">與實驗相關聯的啟動選項。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-118">The start option associated with the experiment.</span></span>

<span data-ttu-id="6d5a0-119">**experimentType**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-119">**experimentType**</span></span>  
<span data-ttu-id="6d5a0-120"> (capture) 的實驗類型。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-120">The kind of experiment (capture).</span></span>

<span data-ttu-id="6d5a0-121">**uiLocale**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-121">**uiLocale**</span></span>  
<span data-ttu-id="6d5a0-122">Experiement (capture) 期間，用於 UI 重迭元素的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-122">The ID of the locale used for UI overlay elements during the experiement (capture).</span></span> <span data-ttu-id="6d5a0-123">這會從主機 (（例如 Visual Studio 圖形診斷) 傳遞至 capture 引擎）。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-123">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

<span data-ttu-id="6d5a0-124">**registryRoot**</span><span class="sxs-lookup"><span data-stu-id="6d5a0-124">**registryRoot**</span></span>  
<span data-ttu-id="6d5a0-125">包含登錄根目錄的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-125">A COM string containing the registry root.</span></span> <span data-ttu-id="6d5a0-126">這會從主機 (（例如 Visual Studio 圖形診斷) 傳遞至 capture 引擎）。</span><span class="sxs-lookup"><span data-stu-id="6d5a0-126">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d5a0-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d5a0-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6d5a0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6d5a0-128">Header</span></span></p></td><td><span data-ttu-id="6d5a0-129">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="6d5a0-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



