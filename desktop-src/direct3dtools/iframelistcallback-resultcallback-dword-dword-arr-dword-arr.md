---
description: 回呼函式，用來通知主控制項已被捕獲的框架。
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameListCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 00a991ec2d380d9c052f02ed69bb71d233fd0d93
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467927"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span data-ttu-id="9ac0f-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="9ac0f-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback::ResultCallback method</span></span>

<span data-ttu-id="9ac0f-104">回呼函式，用來通知主控制項已被捕獲的框架。</span><span class="sxs-lookup"><span data-stu-id="9ac0f-104">A callback function used to notify the host of which frames were captured.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac0f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9ac0f-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a><span data-ttu-id="9ac0f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ac0f-106">Parameters</span></span>

<span data-ttu-id="9ac0f-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="9ac0f-107">*numFrames* </span></span>  
<span data-ttu-id="9ac0f-108">所捕獲的框架數目。</span><span class="sxs-lookup"><span data-stu-id="9ac0f-108">The number of frames captured.</span></span>

<span data-ttu-id="9ac0f-109">*count0 \_ frameNumbers* </span><span class="sxs-lookup"><span data-stu-id="9ac0f-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="9ac0f-110">已捕獲框架的框架編號。</span><span class="sxs-lookup"><span data-stu-id="9ac0f-110">The frame numbers of the captured frames.</span></span>

<span data-ttu-id="9ac0f-111">*count0 \_ frameEventIDs* </span><span class="sxs-lookup"><span data-stu-id="9ac0f-111">*count0\_frameEventIDs* </span></span>  
<span data-ttu-id="9ac0f-112">與每個畫面格相關聯的最後一個事件。</span><span class="sxs-lookup"><span data-stu-id="9ac0f-112">The final event associated with each frame.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ac0f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ac0f-113">Return value</span></span>

<span data-ttu-id="9ac0f-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9ac0f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ac0f-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9ac0f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac0f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ac0f-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9ac0f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="9ac0f-117">Header</span></span></p></td><td><span data-ttu-id="9ac0f-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9ac0f-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9ac0f-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ac0f-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9ac0f-120">**IFrameListCallback**</span><span class="sxs-lookup"><span data-stu-id="9ac0f-120">**IFrameListCallback**</span></span>](/windows/desktop/direct3dtools/iframelistcallback)

 

 
