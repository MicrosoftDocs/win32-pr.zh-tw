---
description: Remove 方法會從時間軸中移除此物件 (包括子物件，而不是子系) ，可供其他地方 reinsertion。
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'IAMTimelineObj：： Remove 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987874"
---
# <a name="iamtimelineobjremove-method"></a><span data-ttu-id="7d69c-103">IAMTimelineObj：： Remove 方法</span><span class="sxs-lookup"><span data-stu-id="7d69c-103">IAMTimelineObj::Remove method</span></span>

> [!Note]  
> <span data-ttu-id="7d69c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7d69c-104">\[Deprecated.</span></span> <span data-ttu-id="7d69c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7d69c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7d69c-106">`Remove`方法會從時間軸中移除此物件 (包括子物件，而不是子系) ，可供其他地方 reinsertion。</span><span class="sxs-lookup"><span data-stu-id="7d69c-106">The `Remove` method removes this object from the timeline (including subobjects but not children), for reinsertion elsewhere.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d69c-107">語法</span><span class="sxs-lookup"><span data-stu-id="7d69c-107">Syntax</span></span>


```C++
HRESULT Remove();
```



## <a name="parameters"></a><span data-ttu-id="7d69c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7d69c-108">Parameters</span></span>

<span data-ttu-id="7d69c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7d69c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d69c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d69c-110">Return value</span></span>

<span data-ttu-id="7d69c-111">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7d69c-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d69c-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7d69c-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d69c-113">備註</span><span class="sxs-lookup"><span data-stu-id="7d69c-113">Remarks</span></span>

<span data-ttu-id="7d69c-114">只有在應用程式會立即將物件插入至時間軸時，才呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7d69c-114">Call this method only if the application will immediately insert the object back into the timeline.</span></span> <span data-ttu-id="7d69c-115">這是不正確作業，無法在不重新插入物件的情況下呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7d69c-115">It is an invalid operation to call this method without then reinserting the object.</span></span> <span data-ttu-id="7d69c-116">若要永久移除物件，請呼叫 [**IAMTimelineObj：： RemoveAll**](iamtimelineobj-removeall.md)。</span><span class="sxs-lookup"><span data-stu-id="7d69c-116">To remove an object permanently, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).</span></span>

> [!Note]  
> <span data-ttu-id="7d69c-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="7d69c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7d69c-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7d69c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7d69c-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="7d69c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d69c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d69c-120">Requirements</span></span>



| <span data-ttu-id="7d69c-121">需求</span><span class="sxs-lookup"><span data-stu-id="7d69c-121">Requirement</span></span> | <span data-ttu-id="7d69c-122">值</span><span class="sxs-lookup"><span data-stu-id="7d69c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d69c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7d69c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7d69c-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d69c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7d69c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d69c-125">Library</span></span><br/> | <dl> <span data-ttu-id="7d69c-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d69c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d69c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d69c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d69c-128">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="7d69c-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="7d69c-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="7d69c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




