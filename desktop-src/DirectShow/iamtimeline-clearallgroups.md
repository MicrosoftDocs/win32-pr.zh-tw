---
description: ClearAllGroups 方法會從時間軸移除所有群組，以及這些群組中包含的所有物件。
ms.assetid: b0d2a463-bd18-4377-893c-ea4fdf77b1c8
title: 'IAMTimeline：： ClearAllGroups 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ClearAllGroups
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05d847bdae9d6f5f5672d555a31505c2739af41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992572"
---
# <a name="iamtimelineclearallgroups-method"></a><span data-ttu-id="e8fb2-103">IAMTimeline：： ClearAllGroups 方法</span><span class="sxs-lookup"><span data-stu-id="e8fb2-103">IAMTimeline::ClearAllGroups method</span></span>

> [!Note]  
> <span data-ttu-id="e8fb2-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-104">\[Deprecated.</span></span> <span data-ttu-id="e8fb2-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e8fb2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e8fb2-106">`ClearAllGroups`方法會從時間軸移除所有群組，以及這些群組中包含的所有物件。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-106">The `ClearAllGroups` method removes all groups from the timeline, along with all objects contained in those groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fb2-107">語法</span><span class="sxs-lookup"><span data-stu-id="e8fb2-107">Syntax</span></span>


```C++
HRESULT ClearAllGroups();
```



## <a name="parameters"></a><span data-ttu-id="e8fb2-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8fb2-108">Parameters</span></span>

<span data-ttu-id="e8fb2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8fb2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8fb2-110">Return value</span></span>

<span data-ttu-id="e8fb2-111">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e8fb2-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8fb2-113">備註</span><span class="sxs-lookup"><span data-stu-id="e8fb2-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8fb2-114">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e8fb2-115">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e8fb2-116">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e8fb2-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8fb2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8fb2-117">Requirements</span></span>



| <span data-ttu-id="e8fb2-118">需求</span><span class="sxs-lookup"><span data-stu-id="e8fb2-118">Requirement</span></span> | <span data-ttu-id="e8fb2-119">值</span><span class="sxs-lookup"><span data-stu-id="e8fb2-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fb2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e8fb2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e8fb2-121"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8fb2-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e8fb2-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="e8fb2-122">Library</span></span><br/> | <dl> <span data-ttu-id="e8fb2-123"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8fb2-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8fb2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8fb2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8fb2-125">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="e8fb2-125">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="e8fb2-126">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="e8fb2-126">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




