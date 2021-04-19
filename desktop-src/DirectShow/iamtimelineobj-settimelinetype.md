---
description: 不支援。 呼叫 IAMTimeline：： CreateEmptyNode 方法，以建立新的時間軸物件。 一旦建立物件之後，您就無法變更其類型。
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'IAMTimelineObj：： SetTimelineType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995396"
---
# <a name="iamtimelineobjsettimelinetype-method"></a><span data-ttu-id="57731-105">IAMTimelineObj：： SetTimelineType 方法</span><span class="sxs-lookup"><span data-stu-id="57731-105">IAMTimelineObj::SetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="57731-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="57731-106">\[Deprecated.</span></span> <span data-ttu-id="57731-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="57731-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="57731-108">不支援。</span><span class="sxs-lookup"><span data-stu-id="57731-108">Not supported.</span></span> <span data-ttu-id="57731-109">呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法，以建立新的時間軸物件。</span><span class="sxs-lookup"><span data-stu-id="57731-109">Call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method to create a new timeline object.</span></span> <span data-ttu-id="57731-110">一旦建立物件之後，您就無法變更其類型。</span><span class="sxs-lookup"><span data-stu-id="57731-110">Once an object is created, you cannot change its type.</span></span>

## <a name="syntax"></a><span data-ttu-id="57731-111">語法</span><span class="sxs-lookup"><span data-stu-id="57731-111">Syntax</span></span>


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a><span data-ttu-id="57731-112">參數</span><span class="sxs-lookup"><span data-stu-id="57731-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57731-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="57731-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="57731-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="57731-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57731-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="57731-115">Return value</span></span>

<span data-ttu-id="57731-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="57731-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57731-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57731-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57731-118">備註</span><span class="sxs-lookup"><span data-stu-id="57731-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="57731-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="57731-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="57731-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="57731-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="57731-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="57731-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57731-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="57731-122">Requirements</span></span>



| <span data-ttu-id="57731-123">需求</span><span class="sxs-lookup"><span data-stu-id="57731-123">Requirement</span></span> | <span data-ttu-id="57731-124">值</span><span class="sxs-lookup"><span data-stu-id="57731-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57731-125">標頭</span><span class="sxs-lookup"><span data-stu-id="57731-125">Header</span></span><br/>  | <dl> <span data-ttu-id="57731-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="57731-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="57731-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="57731-127">Library</span></span><br/> | <dl> <span data-ttu-id="57731-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="57731-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57731-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57731-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57731-130">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="57731-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




