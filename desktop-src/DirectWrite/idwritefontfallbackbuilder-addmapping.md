---
title: IDWriteFontFallbackBuilder AddMapping 方法
description: 將單一對應附加至清單。 針對每個額外的對應呼叫一次。
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- AddMapping 方法直接寫入
- AddMapping 方法 Direct Write，IDWriteFontFallbackBuilder 介面
- IDWriteFontFallbackBuilder 介面 Direct Write，AddMapping 方法
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384921"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a><span data-ttu-id="116e9-107">IDWriteFontFallbackBuilder：： AddMapping 方法</span><span class="sxs-lookup"><span data-stu-id="116e9-107">IDWriteFontFallbackBuilder::AddMapping method</span></span>

<span data-ttu-id="116e9-108">將單一對應附加至清單。</span><span class="sxs-lookup"><span data-stu-id="116e9-108">Appends a single mapping to the list.</span></span> <span data-ttu-id="116e9-109">針對每個額外的對應呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="116e9-109">Call this once for each additional mapping.</span></span>

## <a name="syntax"></a><span data-ttu-id="116e9-110">語法</span><span class="sxs-lookup"><span data-stu-id="116e9-110">Syntax</span></span>


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a><span data-ttu-id="116e9-111">參數</span><span class="sxs-lookup"><span data-stu-id="116e9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="116e9-112">*範圍*</span><span class="sxs-lookup"><span data-stu-id="116e9-112">*ranges*</span></span> 
</dt> <dd>

<span data-ttu-id="116e9-113">類型： \**[**DWRITE \_ UNICODE \_ 範圍**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range) \** _</span><span class="sxs-lookup"><span data-stu-id="116e9-113">Type: \**[**DWRITE\_UNICODE\_RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\** _</span></span>

<span data-ttu-id="116e9-114">適用于此對應的 Unicode 範圍。</span><span class="sxs-lookup"><span data-stu-id="116e9-114">Unicode ranges that apply to this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="116e9-115">_rangesCount \*</span><span class="sxs-lookup"><span data-stu-id="116e9-115">_rangesCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="116e9-116">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="116e9-116">Type: **UINT32**</span></span>

<span data-ttu-id="116e9-117">Unicode 範圍的數目。</span><span class="sxs-lookup"><span data-stu-id="116e9-117">Number of Unicode ranges.</span></span>

</dd> <dt>

<span data-ttu-id="116e9-118">*targetFamilyNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="116e9-118">*targetFamilyNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="116e9-119">Type： **CONST WCHAR \* \***</span><span class="sxs-lookup"><span data-stu-id="116e9-119">Type: **const WCHAR\*\***</span></span>

<span data-ttu-id="116e9-120">目標系列名稱字串的清單。</span><span class="sxs-lookup"><span data-stu-id="116e9-120">List of target family name strings.</span></span>

</dd> <dt>

<span data-ttu-id="116e9-121">*targetFamilyNamesCount*</span><span class="sxs-lookup"><span data-stu-id="116e9-121">*targetFamilyNamesCount*</span></span> 
</dt> <dd>

<span data-ttu-id="116e9-122">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="116e9-122">Type: **UINT32**</span></span>

<span data-ttu-id="116e9-123">目標系列名稱的數目。</span><span class="sxs-lookup"><span data-stu-id="116e9-123">Number of target family names.</span></span>

</dd> <dt>

<span data-ttu-id="116e9-124">*fontCollection* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="116e9-124">*fontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="116e9-125">類型： **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span><span class="sxs-lookup"><span data-stu-id="116e9-125">Type: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span></span>

<span data-ttu-id="116e9-126">這個對應的選擇性明確字型集合。</span><span class="sxs-lookup"><span data-stu-id="116e9-126">Optional explicit font collection for this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="116e9-127">*>localename* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="116e9-127">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="116e9-128">類型： \**CONST WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="116e9-128">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="116e9-129">內容的地區設定。</span><span class="sxs-lookup"><span data-stu-id="116e9-129">Locale of the context.</span></span>

</dd> <dt>

<span data-ttu-id="116e9-130">_baseFamilyName \* \[ in，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="116e9-130">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="116e9-131">類型： \**CONST WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="116e9-131">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="116e9-132">要符合的基底系列名稱（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="116e9-132">Base family name to match against, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="116e9-133">_scale \*</span><span class="sxs-lookup"><span data-stu-id="116e9-133">_scale\*</span></span> 
</dt> <dd>

<span data-ttu-id="116e9-134">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="116e9-134">Type: **FLOAT**</span></span>

<span data-ttu-id="116e9-135">將結果目標字型乘以的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="116e9-135">Scale factor to multiply the result target font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="116e9-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="116e9-136">Return value</span></span>

<span data-ttu-id="116e9-137">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="116e9-137">Type: **HRESULT**</span></span>

<span data-ttu-id="116e9-138">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="116e9-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="116e9-139">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="116e9-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="116e9-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="116e9-140">Requirements</span></span>



| <span data-ttu-id="116e9-141">需求</span><span class="sxs-lookup"><span data-stu-id="116e9-141">Requirement</span></span> | <span data-ttu-id="116e9-142">值</span><span class="sxs-lookup"><span data-stu-id="116e9-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="116e9-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="116e9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="116e9-144">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="116e9-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="116e9-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="116e9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="116e9-146">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="116e9-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="116e9-147">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="116e9-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="116e9-148">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="116e9-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="116e9-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="116e9-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="116e9-150"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="116e9-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="116e9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="116e9-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="116e9-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="116e9-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="116e9-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="116e9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="116e9-154">**IDWriteFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="116e9-154">**IDWriteFontFallbackBuilder**</span></span>](idwritefontfallbackbuilder.md)
</dt> </dl>

 

