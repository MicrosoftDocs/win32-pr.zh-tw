---
description: 以非同步方式將資源傳遞給引擎，例如錯誤訊息的字串。
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine7：： InitEngineAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 21d98a207b0194f281abc2800cd63f9be7de5073
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467919"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span data-ttu-id="d6453-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7：： InitEngineAsync 方法</span><span class="sxs-lookup"><span data-stu-id="d6453-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7::InitEngineAsync method</span></span>

<span data-ttu-id="d6453-104">以非同步方式將資源傳遞給引擎，例如錯誤訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="d6453-104">Asynchronously passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6453-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6453-105">Syntax</span></span>


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d6453-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6453-106">Parameters</span></span>

<span data-ttu-id="d6453-107">*count1 \_ 資源* </span><span class="sxs-lookup"><span data-stu-id="d6453-107">*count1\_resources* </span></span>  
<span data-ttu-id="d6453-108">資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="d6453-108">An array of resources.</span></span>

<span data-ttu-id="d6453-109">*計數* </span><span class="sxs-lookup"><span data-stu-id="d6453-109">*count* </span></span>  
<span data-ttu-id="d6453-110">Count1 資源中的資源數目 \_</span><span class="sxs-lookup"><span data-stu-id="d6453-110">The number of resources in count1\_resources</span></span>

<span data-ttu-id="d6453-111">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="d6453-111">*versionCallback* </span></span>  
<span data-ttu-id="d6453-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="d6453-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="d6453-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="d6453-113">*requestCookie* </span></span>  
<span data-ttu-id="d6453-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="d6453-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d6453-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="d6453-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d6453-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="d6453-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6453-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6453-117">Return value</span></span>

<span data-ttu-id="d6453-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d6453-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6453-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6453-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6453-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6453-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d6453-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d6453-121">Header</span></span></p></td><td><span data-ttu-id="d6453-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="d6453-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d6453-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6453-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d6453-124">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="d6453-124">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
