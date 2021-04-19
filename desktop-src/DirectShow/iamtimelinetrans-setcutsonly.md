---
description: SetCutsOnly 方法會指定是否將轉換轉譯為剪下。 如果是的話，轉換會在剪點立即進行。 如果轉換需要很長的時間才能轉譯，您可能會想要以剪下的速度預覽。
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'IAMTimelineTrans：： SetCutsOnly 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995105"
---
# <a name="iamtimelinetranssetcutsonly-method"></a><span data-ttu-id="ba9ef-105">IAMTimelineTrans：： SetCutsOnly 方法</span><span class="sxs-lookup"><span data-stu-id="ba9ef-105">IAMTimelineTrans::SetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="ba9ef-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-106">\[Deprecated.</span></span> <span data-ttu-id="ba9ef-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ba9ef-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ba9ef-108">`SetCutsOnly`方法會指定轉換是否會轉譯為剪下。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-108">The `SetCutsOnly` method specifies whether the transition is rendered as a cut.</span></span> <span data-ttu-id="ba9ef-109">如果是的話，轉換會在剪點立即進行。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-109">If so, the transition occurs instantly at the cut point.</span></span> <span data-ttu-id="ba9ef-110">如果轉換需要很長的時間才能轉譯，您可能會想要以剪下的速度預覽。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-110">If a transition takes a long time to render, you might want to preview it as a cut to speed preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba9ef-111">語法</span><span class="sxs-lookup"><span data-stu-id="ba9ef-111">Syntax</span></span>


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="ba9ef-112">參數</span><span class="sxs-lookup"><span data-stu-id="ba9ef-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba9ef-113">*Val*</span><span class="sxs-lookup"><span data-stu-id="ba9ef-113">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="ba9ef-114">指定是否要將轉換轉譯為剪下。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-114">Specifies whether to render the transition as a cut.</span></span> <span data-ttu-id="ba9ef-115">若 **為 TRUE**，則轉換會轉譯為瞬間剪下。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-115">If **TRUE**, the transition is rendered as an instantaneous cut.</span></span> <span data-ttu-id="ba9ef-116">如果 **為 FALSE**，則轉換會轉譯為正常持續時間。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-116">If **FALSE**, the transition renders over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba9ef-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba9ef-117">Return value</span></span>

<span data-ttu-id="ba9ef-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba9ef-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba9ef-120">備註</span><span class="sxs-lookup"><span data-stu-id="ba9ef-120">Remarks</span></span>

<span data-ttu-id="ba9ef-121">將轉換轉譯為剪下與交換輸入不相容。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-121">Rendering a transition as a cut is not compatible with swapping the inputs.</span></span> <span data-ttu-id="ba9ef-122"> (請參閱 [**IAMTimelineTrans：： SetSwapInputs**](iamtimelinetrans-setswapinputs.md)) 。如果您呼叫的 `SetCutsOnly` 值為 **TRUE**，它會暫時覆寫 **SetSwapInputs** 設定。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-122">(See [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) If you call `SetCutsOnly` with a value of **TRUE**, it temporarily overrides the **SetSwapInputs** setting.</span></span> <span data-ttu-id="ba9ef-123">僅限剪設定適用于預覽，不過，這項限制不會影響檔案輸出，只要記得 `SetCutsOnly` 在寫入檔案之前，先使用值 **FALSE** 來呼叫。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-123">The cuts-only setting is intended for preview, however, so this limitation does not affect file output—just remember to call `SetCutsOnly` with the value **FALSE** before writing the file.</span></span>

> [!Note]  
> <span data-ttu-id="ba9ef-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ba9ef-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ba9ef-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ba9ef-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba9ef-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba9ef-127">Requirements</span></span>



| <span data-ttu-id="ba9ef-128">需求</span><span class="sxs-lookup"><span data-stu-id="ba9ef-128">Requirement</span></span> | <span data-ttu-id="ba9ef-129">值</span><span class="sxs-lookup"><span data-stu-id="ba9ef-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9ef-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ba9ef-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ba9ef-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba9ef-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ba9ef-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="ba9ef-132">Library</span></span><br/> | <dl> <span data-ttu-id="ba9ef-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba9ef-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba9ef-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba9ef-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba9ef-135">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="ba9ef-135">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="ba9ef-136">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ba9ef-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




