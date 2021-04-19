---
description: Put \_ AlphaRamp 方法會指定 Alpha 曲線的屬性。 Alpha 斜接是調整原始影像中 Alpha 值的百分比。 例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter：:p ut_AlphaRamp 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994902"
---
# <a name="idxtalphasetterput_alpharamp-method"></a><span data-ttu-id="d353b-105">IDxtAlphaSetter：:p 的 \_ AlphaRamp 方法</span><span class="sxs-lookup"><span data-stu-id="d353b-105">IDxtAlphaSetter::put\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="d353b-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d353b-106">\[Deprecated.</span></span> <span data-ttu-id="d353b-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d353b-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d353b-108">`put_AlphaRamp`方法會指定 Alpha 曲線的屬性。</span><span class="sxs-lookup"><span data-stu-id="d353b-108">The `put_AlphaRamp` method specifies the alpha ramp property.</span></span> <span data-ttu-id="d353b-109">Alpha 斜接是調整原始影像中 Alpha 值的百分比。</span><span class="sxs-lookup"><span data-stu-id="d353b-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="d353b-110">例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。</span><span class="sxs-lookup"><span data-stu-id="d353b-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="d353b-111">語法</span><span class="sxs-lookup"><span data-stu-id="d353b-111">Syntax</span></span>


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="d353b-112">參數</span><span class="sxs-lookup"><span data-stu-id="d353b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d353b-113">*Alpha* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d353b-113">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d353b-114">以百分比表示的 Alpha 斜坡。</span><span class="sxs-lookup"><span data-stu-id="d353b-114">The alpha ramp as a percentage.</span></span> <span data-ttu-id="d353b-115">例如，1.0 是100%。</span><span class="sxs-lookup"><span data-stu-id="d353b-115">For example, 1.0 is 100%.</span></span> <span data-ttu-id="d353b-116">若要停用此屬性，請設定負數值。</span><span class="sxs-lookup"><span data-stu-id="d353b-116">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d353b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d353b-117">Return value</span></span>

<span data-ttu-id="d353b-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d353b-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d353b-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d353b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d353b-120">備註</span><span class="sxs-lookup"><span data-stu-id="d353b-120">Remarks</span></span>

<span data-ttu-id="d353b-121">如果您將這個屬性設定為非負數值，您也必須使用負數值來呼叫 **put \_ Alpha** ，以停用 Alpha 屬性。</span><span class="sxs-lookup"><span data-stu-id="d353b-121">If you set this property to a non-negative value, you must also disable the alpha property, by calling **put\_Alpha** with a negative value.</span></span> <span data-ttu-id="d353b-122">否則效果將不會正確呈現。</span><span class="sxs-lookup"><span data-stu-id="d353b-122">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="d353b-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d353b-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d353b-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d353b-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d353b-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d353b-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d353b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d353b-126">Requirements</span></span>



| <span data-ttu-id="d353b-127">需求</span><span class="sxs-lookup"><span data-stu-id="d353b-127">Requirement</span></span> | <span data-ttu-id="d353b-128">值</span><span class="sxs-lookup"><span data-stu-id="d353b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d353b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d353b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d353b-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d353b-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d353b-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d353b-131">Library</span></span><br/> | <dl> <span data-ttu-id="d353b-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d353b-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d353b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d353b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d353b-134">**IDxtAlphaSetter 介面**</span><span class="sxs-lookup"><span data-stu-id="d353b-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="d353b-135">**IDxtAlphaSetter：:p ui \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="d353b-135">**IDxtAlphaSetter::put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




