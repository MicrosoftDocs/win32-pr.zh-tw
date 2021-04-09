---
title: 外掛程式包裝函數
description: 包裝函式，可讓您在任何附加至管線的介面卡上呼叫公用函式，而不需要手動取得介面卡的指標。
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API、外掛程式包裝函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840595"
---
# <a name="plug-in-wrapper-functions"></a><span data-ttu-id="5ebcc-104">外掛程式包裝函數</span><span class="sxs-lookup"><span data-stu-id="5ebcc-104">Plug-in Wrapper Functions</span></span>

<span data-ttu-id="5ebcc-105">Windows 生物特徵辨識架構 API 包含包裝函式，可讓您在任何附加至管線的介面卡上呼叫公用函式，而不需要手動取得介面卡的指標。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-105">The Windows Biometric Framework API includes wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span> <span data-ttu-id="5ebcc-106">每個包裝函式都會檢查輸入引數、抓取介面卡指標，以及呼叫要求的函式。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-106">Each wrapper checks the input arguments, retrieves an adapter pointer, and calls the requested function.</span></span> <span data-ttu-id="5ebcc-107">例如， **WbioEngineSetHashAlgorithm** 包裝函式具有下列簽章。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-107">For example, the **WbioEngineSetHashAlgorithm** wrapper has the following signature.</span></span>


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



<span data-ttu-id="5ebcc-108">此函數會確認 *管線* 引數不是 **Null**、引擎介面卡存在，而且 [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) 函式存在。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-108">The function verifies that the *Pipeline* argument is not **NULL**, that an engine adapter exists, and that the [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) function exists.</span></span> <span data-ttu-id="5ebcc-109">所有包裝函式都是在 Winbio \_ adapter .h 標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-109">All wrapper functions are defined in the Winbio\_adapter.h header file.</span></span> <span data-ttu-id="5ebcc-110">下列主題討論可用的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-110">The following topics discuss the available wrappers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5ebcc-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="5ebcc-111">In this section</span></span>



| <span data-ttu-id="5ebcc-112">主題</span><span class="sxs-lookup"><span data-stu-id="5ebcc-112">Topic</span></span>                                                               | <span data-ttu-id="5ebcc-113">描述</span><span class="sxs-lookup"><span data-stu-id="5ebcc-113">Description</span></span>                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ebcc-114">引擎介面卡包裝函式</span><span class="sxs-lookup"><span data-stu-id="5ebcc-114">Engine Adapter Wrappers</span></span>](engine-adapter-wrappers.md)<br/>   | <span data-ttu-id="5ebcc-115">您可以用來在引擎介面卡上呼叫函式的函式。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-115">Functions that you can use to call functions on your engine adapter.</span></span> <span data-ttu-id="5ebcc-116">這些函式定義于 Winbio \_ adapter. h 中。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-116">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="5ebcc-117">感應器介面卡包裝函式</span><span class="sxs-lookup"><span data-stu-id="5ebcc-117">Sensor Adapter Wrappers</span></span>](sensor-adapter-wrappers.md)<br/>   | <span data-ttu-id="5ebcc-118">您可以用來在感應器介面卡上呼叫函式的函式。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-118">Functions that you can use to call functions on your sensor adapter.</span></span> <span data-ttu-id="5ebcc-119">這些函式定義于 Winbio \_ adapter. h 中。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-119">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="5ebcc-120">儲存體介面卡包裝函式</span><span class="sxs-lookup"><span data-stu-id="5ebcc-120">Storage Adapter Wrappers</span></span>](storage-adapter-wrappers.md)<br/> | <span data-ttu-id="5ebcc-121">您可以用來在儲存體介面卡上呼叫函式的函式。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-121">Functions that you can use to call functions on your storage adapter.</span></span> <span data-ttu-id="5ebcc-122">這些函式定義于 Winbio \_ adapter. h 中。</span><span class="sxs-lookup"><span data-stu-id="5ebcc-122">These functions are defined in Winbio\_adapter.h.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5ebcc-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ebcc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ebcc-124">外掛程式參考</span><span class="sxs-lookup"><span data-stu-id="5ebcc-124">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> </dl>

 

 





