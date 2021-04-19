---
description: VTrackSwapPriorities 方法會切換兩個追蹤的優先權層級。
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'IAMTimelineComp：： VTrackSwapPriorities 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995101"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a><span data-ttu-id="c9148-103">IAMTimelineComp：： VTrackSwapPriorities 方法</span><span class="sxs-lookup"><span data-stu-id="c9148-103">IAMTimelineComp::VTrackSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="c9148-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c9148-104">\[Deprecated.</span></span> <span data-ttu-id="c9148-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c9148-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c9148-106">`VTrackSwapPriorities`方法會切換兩個追蹤的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="c9148-106">The `VTrackSwapPriorities` method switches the priority levels of two tracks.</span></span>

<span data-ttu-id="c9148-107">由於有兩個優先權層級，此方法會將虛擬追蹤切換至這些優先順序。</span><span class="sxs-lookup"><span data-stu-id="c9148-107">Given two priority levels, this method switches the virtual tracks at those priorities.</span></span> <span data-ttu-id="c9148-108">當方法傳回時，位於第一個優先權層級的追蹤現在會在第二個優先權層級，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="c9148-108">When the method returns, the track that was at the first priority level is now at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9148-109">語法</span><span class="sxs-lookup"><span data-stu-id="c9148-109">Syntax</span></span>


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a><span data-ttu-id="c9148-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9148-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9148-111">*VirtualTrackA*</span><span class="sxs-lookup"><span data-stu-id="c9148-111">*VirtualTrackA*</span></span> 
</dt> <dd>

<span data-ttu-id="c9148-112">要交換虛擬追蹤的第一個優先權層級。</span><span class="sxs-lookup"><span data-stu-id="c9148-112">First priority level at which to swap virtual tracks.</span></span>

</dd> <dt>

<span data-ttu-id="c9148-113">*VirtualTrackB*</span><span class="sxs-lookup"><span data-stu-id="c9148-113">*VirtualTrackB*</span></span> 
</dt> <dd>

<span data-ttu-id="c9148-114">要交換虛擬追蹤的第二個優先權等級。</span><span class="sxs-lookup"><span data-stu-id="c9148-114">Second priority level at which to swap virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9148-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9148-115">Return value</span></span>

<span data-ttu-id="c9148-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c9148-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9148-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9148-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9148-118">備註</span><span class="sxs-lookup"><span data-stu-id="c9148-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c9148-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="c9148-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c9148-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c9148-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c9148-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="c9148-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9148-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9148-122">Requirements</span></span>



| <span data-ttu-id="c9148-123">需求</span><span class="sxs-lookup"><span data-stu-id="c9148-123">Requirement</span></span> | <span data-ttu-id="c9148-124">值</span><span class="sxs-lookup"><span data-stu-id="c9148-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9148-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c9148-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c9148-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9148-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c9148-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9148-127">Library</span></span><br/> | <dl> <span data-ttu-id="c9148-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9148-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9148-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9148-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9148-130">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="c9148-130">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="c9148-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="c9148-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




