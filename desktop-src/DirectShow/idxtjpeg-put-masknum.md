---
description: Put \_ MaskNum 方法會指定抹除的 SMPTE 清除程式碼。
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: 'IDxtJpeg：:p ut_MaskNum 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993315"
---
# <a name="idxtjpegput_masknum-method"></a><span data-ttu-id="21a90-103">IDxtJpeg：:p 的 \_ MaskNum 方法</span><span class="sxs-lookup"><span data-stu-id="21a90-103">IDxtJpeg::put\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="21a90-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="21a90-104">\[Deprecated.</span></span> <span data-ttu-id="21a90-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="21a90-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21a90-106">方法會指定抹除的 `put_MaskNum` SMPTE 清除程式碼。</span><span class="sxs-lookup"><span data-stu-id="21a90-106">The `put_MaskNum` method specifies the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a90-107">語法</span><span class="sxs-lookup"><span data-stu-id="21a90-107">Syntax</span></span>


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="21a90-108">參數</span><span class="sxs-lookup"><span data-stu-id="21a90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21a90-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21a90-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21a90-110">指定 SMPTE 清除程式碼。</span><span class="sxs-lookup"><span data-stu-id="21a90-110">Specifies the SMPTE wipe code.</span></span> <span data-ttu-id="21a90-111">如需支援的 SMPTE 清除清單，請參閱 [smpte 抹除轉換](smpte-wipe-transition.md)。</span><span class="sxs-lookup"><span data-stu-id="21a90-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21a90-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="21a90-112">Return value</span></span>

<span data-ttu-id="21a90-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="21a90-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21a90-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="21a90-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21a90-115">備註</span><span class="sxs-lookup"><span data-stu-id="21a90-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="21a90-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="21a90-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="21a90-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="21a90-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="21a90-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="21a90-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21a90-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="21a90-119">Requirements</span></span>



| <span data-ttu-id="21a90-120">需求</span><span class="sxs-lookup"><span data-stu-id="21a90-120">Requirement</span></span> | <span data-ttu-id="21a90-121">值</span><span class="sxs-lookup"><span data-stu-id="21a90-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21a90-122">標頭</span><span class="sxs-lookup"><span data-stu-id="21a90-122">Header</span></span><br/>  | <dl> <span data-ttu-id="21a90-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="21a90-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="21a90-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="21a90-124">Library</span></span><br/> | <dl> <span data-ttu-id="21a90-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21a90-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a90-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21a90-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a90-127">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="21a90-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




