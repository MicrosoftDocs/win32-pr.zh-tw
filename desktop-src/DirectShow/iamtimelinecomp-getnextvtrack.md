---
description: GetNextVTrack 方法會在指定的虛擬追蹤之後，抓取下一個虛擬追蹤。
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'IAMTimelineComp：： GetNextVTrack 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990983"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a><span data-ttu-id="2cbc3-103">IAMTimelineComp：： GetNextVTrack 方法</span><span class="sxs-lookup"><span data-stu-id="2cbc3-103">IAMTimelineComp::GetNextVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="2cbc3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-104">\[Deprecated.</span></span> <span data-ttu-id="2cbc3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2cbc3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2cbc3-106">方法會在 `GetNextVTrack` 指定的虛擬追蹤之後抓取下一個虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-106">The `GetNextVTrack` method retrieves the next virtual track after a specified virtual track.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbc3-107">語法</span><span class="sxs-lookup"><span data-stu-id="2cbc3-107">Syntax</span></span>


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a><span data-ttu-id="2cbc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="2cbc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbc3-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="2cbc3-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbc3-110">先前虛擬追蹤的指標，或為 **Null** ，以取出組合中的第一個虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-110">Pointer to the previous virtual track, or **NULL** to retrieve the first virtual track in the composition.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc3-111">*ppNextVirtualTrack* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2cbc3-111">*ppNextVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbc3-112">以優先權的順序接收下一個虛擬追蹤的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the next virtual track, in order of priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbc3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cbc3-113">Return value</span></span>

<span data-ttu-id="2cbc3-114">\_如果方法抓取虛擬追蹤，則傳回 [確定]， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-114">Returns S\_OK if the method retrieves a virtual track, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbc3-115">備註</span><span class="sxs-lookup"><span data-stu-id="2cbc3-115">Remarks</span></span>

<span data-ttu-id="2cbc3-116">如果方法成功，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-116">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="2cbc3-117">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="2cbc3-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2cbc3-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2cbc3-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2cbc3-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2cbc3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cbc3-121">Requirements</span></span>



| <span data-ttu-id="2cbc3-122">需求</span><span class="sxs-lookup"><span data-stu-id="2cbc3-122">Requirement</span></span> | <span data-ttu-id="2cbc3-123">值</span><span class="sxs-lookup"><span data-stu-id="2cbc3-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbc3-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2cbc3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2cbc3-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc3-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2cbc3-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2cbc3-126">Library</span></span><br/> | <dl> <span data-ttu-id="2cbc3-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc3-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cbc3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cbc3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbc3-129">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="2cbc3-129">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="2cbc3-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2cbc3-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




