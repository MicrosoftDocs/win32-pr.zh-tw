---
description: 用來通知主機呼叫堆疊資訊的回呼函數。
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ICallStackCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846399"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span data-ttu-id="3b576-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="3b576-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback::ResultCallback method</span></span>

<span data-ttu-id="3b576-104">用來通知主機呼叫堆疊資訊的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="3b576-104">A callback function used to notify the host of call stack information.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b576-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b576-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="3b576-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b576-106">Parameters</span></span>

<span data-ttu-id="3b576-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="3b576-107">*count* </span></span>  
<span data-ttu-id="3b576-108">傳回的 framebuffers 呼叫堆疊數目。</span><span class="sxs-lookup"><span data-stu-id="3b576-108">The number of callstack framebuffers returned.</span></span>

<span data-ttu-id="3b576-109">*count0 \_ callStackFrameBuffer* </span><span class="sxs-lookup"><span data-stu-id="3b576-109">*count0\_callStackFrameBuffer* </span></span>  
<span data-ttu-id="3b576-110">呼叫堆疊資訊。</span><span class="sxs-lookup"><span data-stu-id="3b576-110">The callstack information.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b576-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b576-111">Return value</span></span>

<span data-ttu-id="3b576-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3b576-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b576-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b576-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b576-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b576-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3b576-115">標頭</span><span class="sxs-lookup"><span data-stu-id="3b576-115">Header</span></span></p></td><td><span data-ttu-id="3b576-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="3b576-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3b576-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b576-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3b576-118">**ICallStackCallback**</span><span class="sxs-lookup"><span data-stu-id="3b576-118">**ICallStackCallback**</span></span>](/windows/desktop/direct3dtools/icallstackcallback)

 

 
