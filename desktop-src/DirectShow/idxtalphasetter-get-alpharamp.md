---
description: Get \_ AlphaRamp 方法會抓取 Alpha 曲線的屬性。 Alpha 斜接是調整原始影像中 Alpha 值的百分比。 例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'IDxtAlphaSetter：： get_AlphaRamp 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994239"
---
# <a name="idxtalphasetterget_alpharamp-method"></a><span data-ttu-id="ea069-105">IDxtAlphaSetter：： get \_ AlphaRamp 方法</span><span class="sxs-lookup"><span data-stu-id="ea069-105">IDxtAlphaSetter::get\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="ea069-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ea069-106">\[Deprecated.</span></span> <span data-ttu-id="ea069-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ea069-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ea069-108">方法會抓取 `get_AlphaRamp` Alpha 曲線的屬性。</span><span class="sxs-lookup"><span data-stu-id="ea069-108">The `get_AlphaRamp` method retrieves the alpha ramp property.</span></span> <span data-ttu-id="ea069-109">Alpha 斜接是調整原始影像中 Alpha 值的百分比。</span><span class="sxs-lookup"><span data-stu-id="ea069-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="ea069-110">例如，如果 Alpha 的斜坡為0.5，則影像中的 Alpha 值會降低50%。</span><span class="sxs-lookup"><span data-stu-id="ea069-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea069-111">語法</span><span class="sxs-lookup"><span data-stu-id="ea069-111">Syntax</span></span>


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="ea069-112">參數</span><span class="sxs-lookup"><span data-stu-id="ea069-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea069-113">*pAlpha* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="ea069-113">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ea069-114">接收 Alpha 斜坡。</span><span class="sxs-lookup"><span data-stu-id="ea069-114">Receives the alpha ramp.</span></span> <span data-ttu-id="ea069-115">負數值表示未設定 Alpha 斜坡。</span><span class="sxs-lookup"><span data-stu-id="ea069-115">A negative value indicates that no alpha ramp is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea069-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea069-116">Return value</span></span>

<span data-ttu-id="ea069-117">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ea069-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ea069-118">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="ea069-118">Possible values include the following.</span></span>



| <span data-ttu-id="ea069-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea069-119">Return code</span></span>                                                                               | <span data-ttu-id="ea069-120">Description</span><span class="sxs-lookup"><span data-stu-id="ea069-120">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="ea069-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ea069-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ea069-122">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="ea069-122">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="ea069-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ea069-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ea069-124">Success</span><span class="sxs-lookup"><span data-stu-id="ea069-124">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="ea069-125">備註</span><span class="sxs-lookup"><span data-stu-id="ea069-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea069-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ea069-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ea069-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ea069-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ea069-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ea069-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea069-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea069-129">Requirements</span></span>



| <span data-ttu-id="ea069-130">需求</span><span class="sxs-lookup"><span data-stu-id="ea069-130">Requirement</span></span> | <span data-ttu-id="ea069-131">值</span><span class="sxs-lookup"><span data-stu-id="ea069-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea069-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ea069-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ea069-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea069-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ea069-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea069-134">Library</span></span><br/> | <dl> <span data-ttu-id="ea069-135"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea069-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea069-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea069-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea069-137">**IDxtAlphaSetter 介面**</span><span class="sxs-lookup"><span data-stu-id="ea069-137">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




