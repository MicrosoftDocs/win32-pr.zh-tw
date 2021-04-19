---
description: ModifyStopTime2 方法會設定停止時間。 這個方法相當於 IAMTimelineSrc：： ModifyStopTime，但會接受 REFTIME 值。
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'IAMTimelineSrc：： ModifyStopTime2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993643"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a><span data-ttu-id="061bf-104">IAMTimelineSrc：： ModifyStopTime2 方法</span><span class="sxs-lookup"><span data-stu-id="061bf-104">IAMTimelineSrc::ModifyStopTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="061bf-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="061bf-105">\[Deprecated.</span></span> <span data-ttu-id="061bf-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="061bf-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="061bf-107">`ModifyStopTime2`方法會設定停止時間。</span><span class="sxs-lookup"><span data-stu-id="061bf-107">The `ModifyStopTime2` method sets the stop time.</span></span> <span data-ttu-id="061bf-108">這個方法相當於 [**IAMTimelineSrc：： ModifyStopTime**](iamtimelinesrc-modifystoptime.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="061bf-108">This method is equivalent to [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="061bf-109">語法</span><span class="sxs-lookup"><span data-stu-id="061bf-109">Syntax</span></span>


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="061bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="061bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061bf-111">*停止*</span><span class="sxs-lookup"><span data-stu-id="061bf-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="061bf-112">新的停止時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="061bf-112">New stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061bf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="061bf-113">Return value</span></span>

<span data-ttu-id="061bf-114">\_如果成功，則傳回 S OK， \_ 如果指定的時間無效，則傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="061bf-114">Returns S\_OK if successful, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="061bf-115">備註</span><span class="sxs-lookup"><span data-stu-id="061bf-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="061bf-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="061bf-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="061bf-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="061bf-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="061bf-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="061bf-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="061bf-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="061bf-119">Requirements</span></span>



| <span data-ttu-id="061bf-120">需求</span><span class="sxs-lookup"><span data-stu-id="061bf-120">Requirement</span></span> | <span data-ttu-id="061bf-121">值</span><span class="sxs-lookup"><span data-stu-id="061bf-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="061bf-122">標頭</span><span class="sxs-lookup"><span data-stu-id="061bf-122">Header</span></span><br/>  | <dl> <span data-ttu-id="061bf-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="061bf-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="061bf-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="061bf-124">Library</span></span><br/> | <dl> <span data-ttu-id="061bf-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="061bf-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061bf-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="061bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061bf-127">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="061bf-127">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="061bf-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="061bf-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




