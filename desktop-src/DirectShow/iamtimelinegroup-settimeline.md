---
description: 不支援。 請改為呼叫 IAMTimeline：： AddGroup 方法。
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'IAMTimelineGroup：： SetTimeline 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993220"
---
# <a name="iamtimelinegroupsettimeline-method"></a><span data-ttu-id="eb983-104">IAMTimelineGroup：： SetTimeline 方法</span><span class="sxs-lookup"><span data-stu-id="eb983-104">IAMTimelineGroup::SetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="eb983-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="eb983-105">\[Deprecated.</span></span> <span data-ttu-id="eb983-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="eb983-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eb983-107">不支援。</span><span class="sxs-lookup"><span data-stu-id="eb983-107">Not supported.</span></span> <span data-ttu-id="eb983-108">請改為呼叫 [**IAMTimeline：： AddGroup**](iamtimeline-addgroup.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eb983-108">Call the [**IAMTimeline::AddGroup**](iamtimeline-addgroup.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb983-109">語法</span><span class="sxs-lookup"><span data-stu-id="eb983-109">Syntax</span></span>


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="eb983-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb983-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb983-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="eb983-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="eb983-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="eb983-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb983-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb983-113">Return value</span></span>

<span data-ttu-id="eb983-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="eb983-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb983-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eb983-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb983-116">備註</span><span class="sxs-lookup"><span data-stu-id="eb983-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eb983-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="eb983-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb983-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="eb983-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eb983-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="eb983-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb983-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb983-120">Requirements</span></span>



| <span data-ttu-id="eb983-121">需求</span><span class="sxs-lookup"><span data-stu-id="eb983-121">Requirement</span></span> | <span data-ttu-id="eb983-122">值</span><span class="sxs-lookup"><span data-stu-id="eb983-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb983-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eb983-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eb983-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb983-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eb983-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="eb983-125">Library</span></span><br/> | <dl> <span data-ttu-id="eb983-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb983-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb983-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb983-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb983-128">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="eb983-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




