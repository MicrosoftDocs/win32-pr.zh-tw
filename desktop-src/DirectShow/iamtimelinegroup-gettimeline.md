---
description: GetTimeline 方法會抓取此群組所屬的時間軸。
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'IAMTimelineGroup：： GetTimeline 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982633"
---
# <a name="iamtimelinegroupgettimeline-method"></a><span data-ttu-id="86295-103">IAMTimelineGroup：： GetTimeline 方法</span><span class="sxs-lookup"><span data-stu-id="86295-103">IAMTimelineGroup::GetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="86295-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="86295-104">\[Deprecated.</span></span> <span data-ttu-id="86295-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="86295-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="86295-106">方法會抓取 `GetTimeline` 此群組所屬的時間軸。</span><span class="sxs-lookup"><span data-stu-id="86295-106">The `GetTimeline` method retrieves the timeline to which this group belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="86295-107">語法</span><span class="sxs-lookup"><span data-stu-id="86295-107">Syntax</span></span>


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="86295-108">參數</span><span class="sxs-lookup"><span data-stu-id="86295-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86295-109">*ppTimeline* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="86295-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86295-110">接收時間軸的 [**IAMTimeline**](iamtimeline.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="86295-110">Receives the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="86295-111">如果群組不是時間軸的一部分，此值會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="86295-111">If the group is not part of a timeline, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86295-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="86295-112">Return value</span></span>

<span data-ttu-id="86295-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="86295-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86295-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="86295-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="86295-115">備註</span><span class="sxs-lookup"><span data-stu-id="86295-115">Remarks</span></span>

<span data-ttu-id="86295-116">如果 *ppTimeline* 中傳回的值不是 **Null**，則 **IAMTimeline** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="86295-116">If the value returned in *ppTimeline* is not **NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="86295-117">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="86295-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="86295-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="86295-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="86295-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="86295-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="86295-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="86295-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86295-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="86295-121">Requirements</span></span>



| <span data-ttu-id="86295-122">需求</span><span class="sxs-lookup"><span data-stu-id="86295-122">Requirement</span></span> | <span data-ttu-id="86295-123">值</span><span class="sxs-lookup"><span data-stu-id="86295-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86295-124">標頭</span><span class="sxs-lookup"><span data-stu-id="86295-124">Header</span></span><br/>  | <dl> <span data-ttu-id="86295-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="86295-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="86295-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="86295-126">Library</span></span><br/> | <dl> <span data-ttu-id="86295-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="86295-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86295-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86295-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86295-129">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="86295-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="86295-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="86295-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




