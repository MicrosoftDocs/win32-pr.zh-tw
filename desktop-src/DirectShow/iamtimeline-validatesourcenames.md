---
description: ValidateSourceNames 方法會使用媒體定位器來驗證時間軸中的來源名稱。 （選擇性）此方法也會更新找到檔案的任何來源物件。
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'IAMTimeline：： ValidateSourceNames 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976155"
---
# <a name="iamtimelinevalidatesourcenames-method"></a><span data-ttu-id="15300-104">IAMTimeline：： ValidateSourceNames 方法</span><span class="sxs-lookup"><span data-stu-id="15300-104">IAMTimeline::ValidateSourceNames method</span></span>

> [!Note]  
> <span data-ttu-id="15300-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="15300-105">\[Deprecated.</span></span> <span data-ttu-id="15300-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="15300-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="15300-107">`ValidateSourceNames`方法會使用媒體定位器來驗證時間軸中的來源名稱。</span><span class="sxs-lookup"><span data-stu-id="15300-107">The `ValidateSourceNames` method validates source names in the timeline, using the media locator.</span></span> <span data-ttu-id="15300-108">（選擇性）此方法也會更新找到檔案的任何來源物件。</span><span class="sxs-lookup"><span data-stu-id="15300-108">Optionally, this method also updates any source object for which it locates a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="15300-109">語法</span><span class="sxs-lookup"><span data-stu-id="15300-109">Syntax</span></span>


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a><span data-ttu-id="15300-110">參數</span><span class="sxs-lookup"><span data-stu-id="15300-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15300-111">*ValidateFlags*</span><span class="sxs-lookup"><span data-stu-id="15300-111">*ValidateFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="15300-112">指定媒體定位器行為的 [**檔案名驗證旗標**](file-name-validation-flags.md) 的位元組合。</span><span class="sxs-lookup"><span data-stu-id="15300-112">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="15300-113">SFN \_ VALIDATEF \_ REPLACE 和 SFN \_ VALIDATEF \_ CHECK flags 必須存在，否則方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="15300-113">The SFN\_VALIDATEF\_REPLACE and SFN\_VALIDATEF\_CHECK flags must be present, or the method returns E\_INVALIDARG.</span></span>

</dd> <dt>

<span data-ttu-id="15300-114">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="15300-114">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="15300-115">要用來取代預設值之媒體定位器 [**IMediaLocator**](imedialocator.md) 介面的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="15300-115">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="15300-116">若要使用預設媒體定位器，請將此參數的值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15300-116">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="15300-117">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="15300-117">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="15300-118">*NotifyEventHandle*</span><span class="sxs-lookup"><span data-stu-id="15300-118">*NotifyEventHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="15300-119">事件的控制代碼。</span><span class="sxs-lookup"><span data-stu-id="15300-119">Handle to an event.</span></span> <span data-ttu-id="15300-120">方法會在事件完成驗證之後發出信號。</span><span class="sxs-lookup"><span data-stu-id="15300-120">The method signals the event after it has completed the validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15300-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="15300-121">Return value</span></span>

<span data-ttu-id="15300-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="15300-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15300-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="15300-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="15300-124">備註</span><span class="sxs-lookup"><span data-stu-id="15300-124">Remarks</span></span>

<span data-ttu-id="15300-125">使用 *pOverride* 參數，您可以提供自己自訂的 [**IMediaLocator**](imedialocator.md) 介面實作為。</span><span class="sxs-lookup"><span data-stu-id="15300-125">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="15300-126">例如，預設媒體定位器將不會通知您的應用程式 (找到的檔案，或找不到) 。</span><span class="sxs-lookup"><span data-stu-id="15300-126">For example, the default media locator will not notify your application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="15300-127">若要解決這項限制，您可以執行自訂媒體定位器，使其成為預設版本的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="15300-127">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="15300-128">在您的自訂版本中，將 [**IMediaLocator：： FindMediaFile**](imedialocator-findmediafile.md) 呼叫直接傳遞至預設版本，並檢查傳回值。</span><span class="sxs-lookup"><span data-stu-id="15300-128">In your custom version, pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version, and examine the return value.</span></span>

> [!Note]  
> <span data-ttu-id="15300-129">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="15300-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="15300-130">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="15300-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="15300-131">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="15300-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15300-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="15300-132">Requirements</span></span>



| <span data-ttu-id="15300-133">需求</span><span class="sxs-lookup"><span data-stu-id="15300-133">Requirement</span></span> | <span data-ttu-id="15300-134">值</span><span class="sxs-lookup"><span data-stu-id="15300-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15300-135">標頭</span><span class="sxs-lookup"><span data-stu-id="15300-135">Header</span></span><br/>  | <dl> <span data-ttu-id="15300-136"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="15300-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="15300-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="15300-137">Library</span></span><br/> | <dl> <span data-ttu-id="15300-138"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="15300-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15300-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15300-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15300-140">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="15300-140">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="15300-141">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="15300-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




