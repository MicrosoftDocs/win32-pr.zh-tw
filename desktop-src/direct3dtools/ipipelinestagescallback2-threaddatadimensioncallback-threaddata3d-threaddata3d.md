---
description: 回呼，會通知主機相關要求中計算著色器的執行緒和群組數目。
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback2：： ThreadDataDimensionCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a8ee64c863128513563f3ce50dd2bfcdd77714
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385805"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span data-ttu-id="aafd0-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2：： ThreadDataDimensionCallback 方法</span><span class="sxs-lookup"><span data-stu-id="aafd0-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2::ThreadDataDimensionCallback method</span></span>

<span data-ttu-id="aafd0-104">回呼，會通知主機相關要求中計算著色器的執行緒和群組數目。</span><span class="sxs-lookup"><span data-stu-id="aafd0-104">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafd0-105">語法</span><span class="sxs-lookup"><span data-stu-id="aafd0-105">Syntax</span></span>


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a><span data-ttu-id="aafd0-106">參數</span><span class="sxs-lookup"><span data-stu-id="aafd0-106">Parameters</span></span>

<span data-ttu-id="aafd0-107">*threadGroupCount* </span><span class="sxs-lookup"><span data-stu-id="aafd0-107">*threadGroupCount* </span></span>  
<span data-ttu-id="aafd0-108">執行緒群組的多維度計數。</span><span class="sxs-lookup"><span data-stu-id="aafd0-108">The multi-dimensional count of thread groups.</span></span>

<span data-ttu-id="aafd0-109">*threadGroupSize* </span><span class="sxs-lookup"><span data-stu-id="aafd0-109">*threadGroupSize* </span></span>  
<span data-ttu-id="aafd0-110">每個執行緒群組的多維度大小。</span><span class="sxs-lookup"><span data-stu-id="aafd0-110">The multi-dimensional size of each thread group.</span></span>

## <a name="return-value"></a><span data-ttu-id="aafd0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aafd0-111">Return value</span></span>

<span data-ttu-id="aafd0-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="aafd0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aafd0-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aafd0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aafd0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="aafd0-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aafd0-115">標頭</span><span class="sxs-lookup"><span data-stu-id="aafd0-115">Header</span></span></p></td><td><span data-ttu-id="aafd0-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="aafd0-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="aafd0-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="aafd0-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="aafd0-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="aafd0-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
