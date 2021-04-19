---
description: 未實作。
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: 'IAMTimeline：： SetInterestRange 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInterestRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a3c92848380bb71bcdca0e6f6de1069d6eb998a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987121"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="557ce-103">IAMTimeline：： SetInterestRange 方法</span><span class="sxs-lookup"><span data-stu-id="557ce-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="557ce-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="557ce-104">\[Deprecated.</span></span> <span data-ttu-id="557ce-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="557ce-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="557ce-106">未實作。</span><span class="sxs-lookup"><span data-stu-id="557ce-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="557ce-107">語法</span><span class="sxs-lookup"><span data-stu-id="557ce-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="557ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="557ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="557ce-109">*開始*</span><span class="sxs-lookup"><span data-stu-id="557ce-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="557ce-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="557ce-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="557ce-111">*停止*</span><span class="sxs-lookup"><span data-stu-id="557ce-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="557ce-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="557ce-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="557ce-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="557ce-113">Return value</span></span>

<span data-ttu-id="557ce-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="557ce-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="557ce-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="557ce-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="557ce-116">備註</span><span class="sxs-lookup"><span data-stu-id="557ce-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="557ce-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="557ce-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="557ce-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="557ce-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="557ce-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="557ce-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="557ce-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="557ce-120">Requirements</span></span>



| <span data-ttu-id="557ce-121">需求</span><span class="sxs-lookup"><span data-stu-id="557ce-121">Requirement</span></span> | <span data-ttu-id="557ce-122">值</span><span class="sxs-lookup"><span data-stu-id="557ce-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="557ce-123">標頭</span><span class="sxs-lookup"><span data-stu-id="557ce-123">Header</span></span><br/>  | <dl> <span data-ttu-id="557ce-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="557ce-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="557ce-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="557ce-125">Library</span></span><br/> | <dl> <span data-ttu-id="557ce-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="557ce-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="557ce-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="557ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557ce-128">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="557ce-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




