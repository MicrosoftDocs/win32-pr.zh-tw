---
description: SetSourceNameValidation 方法會指定轉譯引擎如何驗證檔案名。
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'IRenderEngine：： SetSourceNameValidation 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990935"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a><span data-ttu-id="c7b08-103">IRenderEngine：： SetSourceNameValidation 方法</span><span class="sxs-lookup"><span data-stu-id="c7b08-103">IRenderEngine::SetSourceNameValidation method</span></span>

> [!Note]  
> <span data-ttu-id="c7b08-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c7b08-104">\[Deprecated.</span></span> <span data-ttu-id="c7b08-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c7b08-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c7b08-106">`SetSourceNameValidation`方法會指定轉譯引擎如何驗證檔案名。</span><span class="sxs-lookup"><span data-stu-id="c7b08-106">The `SetSourceNameValidation` method specifies how the render engine validates file names.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b08-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7b08-107">Syntax</span></span>


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a><span data-ttu-id="c7b08-108">參數</span><span class="sxs-lookup"><span data-stu-id="c7b08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b08-109">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="c7b08-109">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b08-110">包含篩選字串配對的 **BSTR** 值，格式為 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrFilter** 成員所需。</span><span class="sxs-lookup"><span data-stu-id="c7b08-110">**BSTR** value containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="c7b08-111">如果媒體定位器向終端使用者顯示 [開啟檔案] 對話方塊，則會使用此篩選器。</span><span class="sxs-lookup"><span data-stu-id="c7b08-111">The media locator uses this filter if it presents an Open File dialog box to the end user.</span></span>

</dd> <dt>

<span data-ttu-id="c7b08-112">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="c7b08-112">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b08-113">要用來取代預設值之媒體定位器 [**IMediaLocator**](imedialocator.md) 介面的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="c7b08-113">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="c7b08-114">若要使用預設媒體定位器，請將此參數的值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c7b08-114">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="c7b08-115">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="c7b08-115">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c7b08-116">*旗標*</span><span class="sxs-lookup"><span data-stu-id="c7b08-116">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b08-117">指定媒體定位器行為的 [**檔案名驗證旗標**](file-name-validation-flags.md) 的位元組合。</span><span class="sxs-lookup"><span data-stu-id="c7b08-117">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="c7b08-118">\_ \_ 必須要有 SFN VALIDATEF 檢查旗標。</span><span class="sxs-lookup"><span data-stu-id="c7b08-118">The SFN\_VALIDATEF\_CHECK flag must be present.</span></span> <span data-ttu-id="c7b08-119">\_ \_ 使用這個方法時，SFN VALIDATEF hlinkMUTED 旗標沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="c7b08-119">The SFN\_VALIDATEF\_hlinkMUTED flag has no effect with this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b08-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7b08-120">Return value</span></span>

<span data-ttu-id="c7b08-121">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="c7b08-121">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="c7b08-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c7b08-122">Return code</span></span>                                                                                            | <span data-ttu-id="c7b08-123">Description</span><span class="sxs-lookup"><span data-stu-id="c7b08-123">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c7b08-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c7b08-124"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="c7b08-125">成功。</span><span class="sxs-lookup"><span data-stu-id="c7b08-125">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="c7b08-126"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7b08-126"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="c7b08-127">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="c7b08-127">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7b08-128">備註</span><span class="sxs-lookup"><span data-stu-id="c7b08-128">Remarks</span></span>

<span data-ttu-id="c7b08-129">使用 *pOverride* 參數，您可以提供自己自訂的 [**IMediaLocator**](imedialocator.md) 介面實作為。</span><span class="sxs-lookup"><span data-stu-id="c7b08-129">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="c7b08-130">例如，預設媒體定位程式不會通知應用程式找到 (的檔案，或找不到) 。</span><span class="sxs-lookup"><span data-stu-id="c7b08-130">For example, the default media locator does not notify an application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="c7b08-131">若要解決這項限制，您可以執行自訂媒體定位器，使其成為預設版本的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="c7b08-131">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="c7b08-132">然後，將 [**IMediaLocator：： FindMediaFile**](imedialocator-findmediafile.md) 呼叫直接傳遞至預設版本，並檢查傳回值。</span><span class="sxs-lookup"><span data-stu-id="c7b08-132">Then pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version and examine the return value.</span></span>

<span data-ttu-id="c7b08-133">目前，這個方法不會驗證動態載入的來源。</span><span class="sxs-lookup"><span data-stu-id="c7b08-133">Currently, this method does not validate dynamically loaded sources.</span></span> <span data-ttu-id="c7b08-134">請參閱 [**IRenderEngine：： SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)。</span><span class="sxs-lookup"><span data-stu-id="c7b08-134">See [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="c7b08-135">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="c7b08-135">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7b08-136">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c7b08-136">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c7b08-137">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="c7b08-137">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7b08-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7b08-138">Requirements</span></span>



| <span data-ttu-id="c7b08-139">需求</span><span class="sxs-lookup"><span data-stu-id="c7b08-139">Requirement</span></span> | <span data-ttu-id="c7b08-140">值</span><span class="sxs-lookup"><span data-stu-id="c7b08-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b08-141">標頭</span><span class="sxs-lookup"><span data-stu-id="c7b08-141">Header</span></span><br/>  | <dl> <span data-ttu-id="c7b08-142"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7b08-142"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c7b08-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7b08-143">Library</span></span><br/> | <dl> <span data-ttu-id="c7b08-144"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7b08-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7b08-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7b08-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b08-146">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="c7b08-146">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="c7b08-147">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="c7b08-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
