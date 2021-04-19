---
description: SetDefaultFPS 方法會設定來源物件的預設畫面播放速率。
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'IAMTimelineSrc：： SetDefaultFPS 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983113"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a><span data-ttu-id="a1ddf-103">IAMTimelineSrc：： SetDefaultFPS 方法</span><span class="sxs-lookup"><span data-stu-id="a1ddf-103">IAMTimelineSrc::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="a1ddf-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-104">\[Deprecated.</span></span> <span data-ttu-id="a1ddf-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="a1ddf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a1ddf-106">`SetDefaultFPS`方法會設定來源物件的預設畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-106">The `SetDefaultFPS` method sets the source object's default frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ddf-107">語法</span><span class="sxs-lookup"><span data-stu-id="a1ddf-107">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="a1ddf-108">參數</span><span class="sxs-lookup"><span data-stu-id="a1ddf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1ddf-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="a1ddf-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="a1ddf-110">預設畫面播放速率（以每秒畫面格速率為單位）。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-110">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1ddf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1ddf-111">Return value</span></span>

<span data-ttu-id="a1ddf-112">\_如果成功，則傳回 S OK， \_ 如果指定的畫面播放速率小於零，則傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-112">Returns S\_OK if successful, or E\_INVALIDARG if the specified frame rate is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ddf-113">備註</span><span class="sxs-lookup"><span data-stu-id="a1ddf-113">Remarks</span></span>

<span data-ttu-id="a1ddf-114">如果轉譯引擎無法從原始來源檔案判斷畫面播放速率，則會使用此值。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-114">The render engine uses this value if it cannot determine the frame rate from the original source file.</span></span>

<span data-ttu-id="a1ddf-115">請僅針對原始程式檔呼叫這個方法，而不使用預先定義的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-115">Call this method only for source files without a predefined frame rate.</span></span> <span data-ttu-id="a1ddf-116">若是點陣圖和 JPEG 檔案，預設畫面播放速率是零，這會導致來源轉譯為靜止影像。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-116">For bitmap and JPEG files, the default frame rate is zero, which causes the source to be rendered as a still image.</span></span> <span data-ttu-id="a1ddf-117">若要使用影像做為 DIB 順序中的第一個畫面格，請將畫面播放速率設定為大於零的值。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-117">To use the image as the first frame in a DIB sequence set the frame rate to a value greater than zero.</span></span> <span data-ttu-id="a1ddf-118">如需詳細資訊，請參閱 [使用來源](working-with-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-118">For more information, see [Working with Sources](working-with-sources.md).</span></span>

> [!Note]  
> <span data-ttu-id="a1ddf-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a1ddf-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1ddf-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="a1ddf-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1ddf-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1ddf-122">Requirements</span></span>



| <span data-ttu-id="a1ddf-123">需求</span><span class="sxs-lookup"><span data-stu-id="a1ddf-123">Requirement</span></span> | <span data-ttu-id="a1ddf-124">值</span><span class="sxs-lookup"><span data-stu-id="a1ddf-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ddf-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a1ddf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a1ddf-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1ddf-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a1ddf-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1ddf-127">Library</span></span><br/> | <dl> <span data-ttu-id="a1ddf-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1ddf-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1ddf-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1ddf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1ddf-130">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="a1ddf-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="a1ddf-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="a1ddf-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




