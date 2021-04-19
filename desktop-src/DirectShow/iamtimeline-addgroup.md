---
description: AddGroup 方法會將群組新增至時間軸。
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'IAMTimeline：： AddGroup 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984018"
---
# <a name="iamtimelineaddgroup-method"></a><span data-ttu-id="551f0-103">IAMTimeline：： AddGroup 方法</span><span class="sxs-lookup"><span data-stu-id="551f0-103">IAMTimeline::AddGroup method</span></span>

> [!Note]  
> <span data-ttu-id="551f0-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="551f0-104">\[Deprecated.</span></span> <span data-ttu-id="551f0-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="551f0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="551f0-106">`AddGroup`方法會將群組新增至時間軸。</span><span class="sxs-lookup"><span data-stu-id="551f0-106">The `AddGroup` method adds a group to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="551f0-107">語法</span><span class="sxs-lookup"><span data-stu-id="551f0-107">Syntax</span></span>


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="551f0-108">參數</span><span class="sxs-lookup"><span data-stu-id="551f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="551f0-109">*pGroup*</span><span class="sxs-lookup"><span data-stu-id="551f0-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="551f0-110">群組之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="551f0-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="551f0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="551f0-111">Return value</span></span>

<span data-ttu-id="551f0-112">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="551f0-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="551f0-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="551f0-113">Return code</span></span>                                                                                   | <span data-ttu-id="551f0-114">Description</span><span class="sxs-lookup"><span data-stu-id="551f0-114">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="551f0-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="551f0-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="551f0-116">成功。</span><span class="sxs-lookup"><span data-stu-id="551f0-116">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="551f0-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="551f0-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="551f0-118">已超過群組的最大數目。</span><span class="sxs-lookup"><span data-stu-id="551f0-118">Maximum number of groups exceeded.</span></span><br/> |
| <dl> <span data-ttu-id="551f0-119"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="551f0-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="551f0-120">物件不是群組。</span><span class="sxs-lookup"><span data-stu-id="551f0-120">The object is not a group.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="551f0-121">備註</span><span class="sxs-lookup"><span data-stu-id="551f0-121">Remarks</span></span>

<span data-ttu-id="551f0-122">目前，時程表最多支援32個群組。</span><span class="sxs-lookup"><span data-stu-id="551f0-122">Currently, timelines support a maximum of 32 groups.</span></span>

> [!Note]  
> <span data-ttu-id="551f0-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="551f0-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="551f0-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="551f0-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="551f0-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="551f0-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="551f0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="551f0-126">Requirements</span></span>



| <span data-ttu-id="551f0-127">需求</span><span class="sxs-lookup"><span data-stu-id="551f0-127">Requirement</span></span> | <span data-ttu-id="551f0-128">值</span><span class="sxs-lookup"><span data-stu-id="551f0-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="551f0-129">標頭</span><span class="sxs-lookup"><span data-stu-id="551f0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="551f0-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="551f0-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="551f0-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="551f0-131">Library</span></span><br/> | <dl> <span data-ttu-id="551f0-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="551f0-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="551f0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="551f0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551f0-134">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="551f0-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="551f0-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="551f0-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




