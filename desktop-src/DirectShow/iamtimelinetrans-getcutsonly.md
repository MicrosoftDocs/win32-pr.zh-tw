---
description: GetCutsOnly 方法會判斷轉換是否轉譯為剪下。 如果是的話，轉換會立即在剪下進行。
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'IAMTimelineTrans：： GetCutsOnly 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001939"
---
# <a name="iamtimelinetransgetcutsonly-method"></a><span data-ttu-id="4783a-104">IAMTimelineTrans：： GetCutsOnly 方法</span><span class="sxs-lookup"><span data-stu-id="4783a-104">IAMTimelineTrans::GetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="4783a-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4783a-105">\[Deprecated.</span></span> <span data-ttu-id="4783a-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4783a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4783a-107">`GetCutsOnly`方法會判斷轉換是否轉譯為剪下。</span><span class="sxs-lookup"><span data-stu-id="4783a-107">The `GetCutsOnly` method determines whether the transition is rendered as a cut.</span></span> <span data-ttu-id="4783a-108">如果是的話，轉換會立即在剪下進行。</span><span class="sxs-lookup"><span data-stu-id="4783a-108">If so, the transition occurs instantaneously at the cut point.</span></span>

## <a name="syntax"></a><span data-ttu-id="4783a-109">語法</span><span class="sxs-lookup"><span data-stu-id="4783a-109">Syntax</span></span>


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4783a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4783a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4783a-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="4783a-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="4783a-112">接收布林值，指定轉換是否轉譯為剪下。</span><span class="sxs-lookup"><span data-stu-id="4783a-112">Receives a Boolean value specifying whether the transition is rendered as a cut.</span></span> <span data-ttu-id="4783a-113">若 **為 TRUE**，則轉換是瞬間剪下。</span><span class="sxs-lookup"><span data-stu-id="4783a-113">If **TRUE**, the transition is an instantaneous cut.</span></span> <span data-ttu-id="4783a-114">如果 **為 FALSE**，則轉換會在其正常持續時間內進行。</span><span class="sxs-lookup"><span data-stu-id="4783a-114">If **FALSE**, the transition occurs over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4783a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4783a-115">Return value</span></span>

<span data-ttu-id="4783a-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4783a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4783a-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4783a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4783a-118">備註</span><span class="sxs-lookup"><span data-stu-id="4783a-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4783a-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4783a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4783a-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4783a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4783a-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4783a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4783a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4783a-122">Requirements</span></span>



| <span data-ttu-id="4783a-123">需求</span><span class="sxs-lookup"><span data-stu-id="4783a-123">Requirement</span></span> | <span data-ttu-id="4783a-124">值</span><span class="sxs-lookup"><span data-stu-id="4783a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4783a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4783a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4783a-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4783a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4783a-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="4783a-127">Library</span></span><br/> | <dl> <span data-ttu-id="4783a-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4783a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4783a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4783a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4783a-130">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="4783a-130">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="4783a-131">**IAMTimelineTrans::SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="4783a-131">**IAMTimelineTrans::SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[<span data-ttu-id="4783a-132">**IAMTimelineTrans::GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="4783a-132">**IAMTimelineTrans::GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[<span data-ttu-id="4783a-133">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4783a-133">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="4783a-134">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4783a-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




