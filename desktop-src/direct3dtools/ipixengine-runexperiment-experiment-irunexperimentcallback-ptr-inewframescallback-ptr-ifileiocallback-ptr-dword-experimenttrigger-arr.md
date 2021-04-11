---
description: 執行實驗。
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine：： RunExperiment 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c656d57dda496b6c1d8c128dc5e832ec40ef13f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109056"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span data-ttu-id="3e825-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine：： RunExperiment 方法</span><span class="sxs-lookup"><span data-stu-id="3e825-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine::RunExperiment method</span></span>

<span data-ttu-id="3e825-104">執行實驗。</span><span class="sxs-lookup"><span data-stu-id="3e825-104">Runs an experiment.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e825-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e825-105">Syntax</span></span>


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="3e825-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e825-106">Parameters</span></span>

<span data-ttu-id="3e825-107">*實驗* </span><span class="sxs-lookup"><span data-stu-id="3e825-107">*experiment* </span></span>  
<span data-ttu-id="3e825-108">描述要執行的實驗。</span><span class="sxs-lookup"><span data-stu-id="3e825-108">Describes the experiment to be run.</span></span>

<span data-ttu-id="3e825-109">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="3e825-109">*pRequestCallback* </span></span>  
<span data-ttu-id="3e825-110">用來通知主機引擎已啟動實驗的函式位址。</span><span class="sxs-lookup"><span data-stu-id="3e825-110">The address of a function used to notify the host that engine has started the experiment.</span></span>

<span data-ttu-id="3e825-111">*回檔* </span><span class="sxs-lookup"><span data-stu-id="3e825-111">*callbacks* </span></span>  
<span data-ttu-id="3e825-112">用來通知主機新框架已被捕獲的函式位址。</span><span class="sxs-lookup"><span data-stu-id="3e825-112">The address of a function used to notify the host that new frames have been captured.</span></span>

<span data-ttu-id="3e825-113">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="3e825-113">*pFileIOCallback* </span></span>  
<span data-ttu-id="3e825-114">用來在剖析期間通知主機檔案 IO 錯誤的函式位址。</span><span class="sxs-lookup"><span data-stu-id="3e825-114">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="3e825-115">*triggersCount* </span><span class="sxs-lookup"><span data-stu-id="3e825-115">*triggersCount* </span></span>  
<span data-ttu-id="3e825-116">實驗中的觸發程式數目。</span><span class="sxs-lookup"><span data-stu-id="3e825-116">The number of triggers in the experiment.</span></span>

<span data-ttu-id="3e825-117">*count4 \_ triggersBuffer* </span><span class="sxs-lookup"><span data-stu-id="3e825-117">*count4\_triggersBuffer* </span></span>  
<span data-ttu-id="3e825-118">捕捉觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3e825-118">Capture triggers.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e825-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e825-119">Return value</span></span>

<span data-ttu-id="3e825-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3e825-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e825-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3e825-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e825-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e825-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3e825-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3e825-123">Header</span></span></p></td><td><span data-ttu-id="3e825-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="3e825-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3e825-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e825-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3e825-126">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="3e825-126">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
