---
description: 回呼，會通知主機相關要求的進度。
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixProgressCallback：:P rogress 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385725"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span data-ttu-id="15fd6-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback：:P rogress 方法</span><span class="sxs-lookup"><span data-stu-id="15fd6-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::Progress method</span></span>

<span data-ttu-id="15fd6-104">回呼，會通知主機相關要求的進度。</span><span class="sxs-lookup"><span data-stu-id="15fd6-104">A callback that notifies the host of the progress of an associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fd6-105">語法</span><span class="sxs-lookup"><span data-stu-id="15fd6-105">Syntax</span></span>


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a><span data-ttu-id="15fd6-106">參數</span><span class="sxs-lookup"><span data-stu-id="15fd6-106">Parameters</span></span>

<span data-ttu-id="15fd6-107">*當前* </span><span class="sxs-lookup"><span data-stu-id="15fd6-107">*current* </span></span>  
<span data-ttu-id="15fd6-108">要求的部分已完成，作為已完成步驟數目的計數。</span><span class="sxs-lookup"><span data-stu-id="15fd6-108">The portion of a request completed, as a count of the number of steps completed.</span></span>

<span data-ttu-id="15fd6-109">*maxSize* </span><span class="sxs-lookup"><span data-stu-id="15fd6-109">*maxSize* </span></span>  
<span data-ttu-id="15fd6-110">完成要求的步驟總數。</span><span class="sxs-lookup"><span data-stu-id="15fd6-110">The total number of steps to complete the request.</span></span>

## <a name="return-value"></a><span data-ttu-id="15fd6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="15fd6-111">Return value</span></span>

<span data-ttu-id="15fd6-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="15fd6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15fd6-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="15fd6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="15fd6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="15fd6-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="15fd6-115">標頭</span><span class="sxs-lookup"><span data-stu-id="15fd6-115">Header</span></span></p></td><td><span data-ttu-id="15fd6-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="15fd6-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="15fd6-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="15fd6-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="15fd6-118">**IPixProgressCallback**</span><span class="sxs-lookup"><span data-stu-id="15fd6-118">**IPixProgressCallback**</span></span>](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
