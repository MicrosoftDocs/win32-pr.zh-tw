---
title: IAMWMBufferPass SetNotify 方法
description: 應用程式會使用 SetNotify 方法，以應用程式的 IAMWMBufferPassCallback 介面指標提供 WM ASF 寫入器或 WM ASF 讀取器篩選器。
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- SetNotify 方法 windows Media 格式
- SetNotify 方法 windows Media Format，IAMWMBufferPass 介面
- IAMWMBufferPass 介面 windows Media Format，SetNotify 方法
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382530"
---
# <a name="iamwmbufferpasssetnotify-method"></a><span data-ttu-id="c8d41-106">IAMWMBufferPass：： SetNotify 方法</span><span class="sxs-lookup"><span data-stu-id="c8d41-106">IAMWMBufferPass::SetNotify method</span></span>

<span data-ttu-id="c8d41-107">應用程式會使用 **SetNotify** 方法，以應用程式的 [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)介面指標提供 wm Asf 寫入器或 [WM asf 讀取](wm-asf-reader-filter.md)器篩選器。</span><span class="sxs-lookup"><span data-stu-id="c8d41-107">The **SetNotify** method is used by applications to provide the WM ASF Writer or [WM ASF Reader](wm-asf-reader-filter.md) filter with a pointer to the application's [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d41-108">語法</span><span class="sxs-lookup"><span data-stu-id="c8d41-108">Syntax</span></span>


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="c8d41-109">參數</span><span class="sxs-lookup"><span data-stu-id="c8d41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d41-110">*pCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8d41-110">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d41-111">應用程式 **IAMWMBufferPassCallback** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c8d41-111">Pointer to the application's **IAMWMBufferPassCallback** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d41-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8d41-112">Return value</span></span>

<span data-ttu-id="c8d41-113">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c8d41-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c8d41-114">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c8d41-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8d41-115">備註</span><span class="sxs-lookup"><span data-stu-id="c8d41-115">Remarks</span></span>

<span data-ttu-id="c8d41-116">請先呼叫這個方法，然後再將篩選圖形置於執行狀態。</span><span class="sxs-lookup"><span data-stu-id="c8d41-116">Call this method before putting the filter graph into the run state.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8d41-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8d41-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d41-118">**IAMWMBufferPass 介面**</span><span class="sxs-lookup"><span data-stu-id="c8d41-118">**IAMWMBufferPass Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 