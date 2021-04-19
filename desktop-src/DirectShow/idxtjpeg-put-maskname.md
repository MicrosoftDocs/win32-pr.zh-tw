---
description: Put \_ MaskName 方法會指定要用作抹除遮罩的 JPEG 檔案名。
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'IDxtJpeg：:p ut_MaskName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976122"
---
# <a name="idxtjpegput_maskname-method"></a><span data-ttu-id="fb070-103">IDxtJpeg：:p 的 \_ MaskName 方法</span><span class="sxs-lookup"><span data-stu-id="fb070-103">IDxtJpeg::put\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="fb070-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fb070-104">\[Deprecated.</span></span> <span data-ttu-id="fb070-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fb070-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fb070-106">`put_MaskName`方法會指定要用作抹除遮罩的 JPEG 檔案名。</span><span class="sxs-lookup"><span data-stu-id="fb070-106">The `put_MaskName` method specifies the name of a JPEG file to use as the wipe mask.</span></span> <span data-ttu-id="fb070-107">將使用這個遮罩，而不是其中一個內建的抹除遮罩。</span><span class="sxs-lookup"><span data-stu-id="fb070-107">This mask will be used instead of one of the built-in wipe masks.</span></span> <span data-ttu-id="fb070-108">檔案必須包含單色、每圖元8位的漸層。</span><span class="sxs-lookup"><span data-stu-id="fb070-108">The file must contain a monochrome, 8-bits-per-pixel gradient.</span></span> <span data-ttu-id="fb070-109">漸層會用來做為遮罩來定義抹除的進度。</span><span class="sxs-lookup"><span data-stu-id="fb070-109">The gradient is used as a mask to define the wipe's progression.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb070-110">語法</span><span class="sxs-lookup"><span data-stu-id="fb070-110">Syntax</span></span>


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fb070-111">參數</span><span class="sxs-lookup"><span data-stu-id="fb070-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb070-112">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb070-112">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb070-113">指定檔案名。</span><span class="sxs-lookup"><span data-stu-id="fb070-113">Specifies the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb070-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb070-114">Return value</span></span>

<span data-ttu-id="fb070-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fb070-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb070-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fb070-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb070-117">備註</span><span class="sxs-lookup"><span data-stu-id="fb070-117">Remarks</span></span>

<span data-ttu-id="fb070-118">若要還原成內建的遮罩，請設定 **MaskNum** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fb070-118">To revert to a built-in mask, set the **MaskNum** property.</span></span>

> [!Note]  
> <span data-ttu-id="fb070-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fb070-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb070-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fb070-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fb070-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fb070-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb070-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb070-122">Requirements</span></span>



| <span data-ttu-id="fb070-123">需求</span><span class="sxs-lookup"><span data-stu-id="fb070-123">Requirement</span></span> | <span data-ttu-id="fb070-124">值</span><span class="sxs-lookup"><span data-stu-id="fb070-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb070-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fb070-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fb070-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb070-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fb070-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb070-127">Library</span></span><br/> | <dl> <span data-ttu-id="fb070-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb070-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb070-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb070-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb070-130">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="fb070-130">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="fb070-131">**IDxtJpeg：:p 的 \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="fb070-131">**IDxtJpeg::put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




