---
description: GetDuration2 方法會抓取時間軸的持續時間。 這個方法相當於 IAMTimeline：： GetDuration，但會採用 double 類型的參數。
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'IAMTimeline：： GetDuration2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995343"
---
# <a name="iamtimelinegetduration2-method"></a><span data-ttu-id="d2d3c-104">IAMTimeline：： GetDuration2 方法</span><span class="sxs-lookup"><span data-stu-id="d2d3c-104">IAMTimeline::GetDuration2 method</span></span>

> [!Note]  
> <span data-ttu-id="d2d3c-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-105">\[Deprecated.</span></span> <span data-ttu-id="d2d3c-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d2d3c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2d3c-107">方法會抓取 `GetDuration2` 時間軸的持續時間。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-107">The `GetDuration2` method retrieves the duration of the timeline.</span></span> <span data-ttu-id="d2d3c-108">這個方法相當於 [**IAMTimeline：： GetDuration**](iamtimeline-getduration.md)，但會採用 **double** 類型的參數。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-108">This method is equivalent to [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), but takes a parameter of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d3c-109">語法</span><span class="sxs-lookup"><span data-stu-id="d2d3c-109">Syntax</span></span>


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="d2d3c-110">參數</span><span class="sxs-lookup"><span data-stu-id="d2d3c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d3c-111">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="d2d3c-111">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d3c-112">接收時間軸的持續時間（以小數秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-112">Receives the duration of the timeline, in fractional seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d3c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2d3c-113">Return value</span></span>

<span data-ttu-id="d2d3c-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2d3c-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2d3c-116">備註</span><span class="sxs-lookup"><span data-stu-id="d2d3c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2d3c-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2d3c-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d2d3c-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d2d3c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2d3c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2d3c-120">Requirements</span></span>



| <span data-ttu-id="d2d3c-121">需求</span><span class="sxs-lookup"><span data-stu-id="d2d3c-121">Requirement</span></span> | <span data-ttu-id="d2d3c-122">值</span><span class="sxs-lookup"><span data-stu-id="d2d3c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d3c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d2d3c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d2d3c-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d3c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d2d3c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2d3c-125">Library</span></span><br/> | <dl> <span data-ttu-id="d2d3c-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2d3c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d3c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2d3c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d3c-128">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="d2d3c-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="d2d3c-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d2d3c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




