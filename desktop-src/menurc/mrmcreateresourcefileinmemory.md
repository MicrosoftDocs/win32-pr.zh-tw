---
title: 'MrmCreateResourceFileInMemory 函式 (MrmResourceIndexer) '
description: 將 PRI 資訊建立為記憶體中的 blob，而不是磁片上的檔案。
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- MrmCreateResourceFileInMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466597"
---
# <a name="mrmcreateresourcefileinmemory-function"></a><span data-ttu-id="ecb88-104">MrmCreateResourceFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="ecb88-104">MrmCreateResourceFileInMemory function</span></span>

<span data-ttu-id="ecb88-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ecb88-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ecb88-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ecb88-107">將 PRI 資訊建立為記憶體中的 blob，而不是磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="ecb88-107">Creates PRI info as a blob in memory, not as a file on disk.</span></span> <span data-ttu-id="ecb88-108">此函式會配置記憶體，並將指標傳回至 *outputPriData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="ecb88-108">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="ecb88-109">使用相同的指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) 來釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="ecb88-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="ecb88-110">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="ecb88-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb88-111">語法</span><span class="sxs-lookup"><span data-stu-id="ecb88-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a><span data-ttu-id="ecb88-112">參數</span><span class="sxs-lookup"><span data-stu-id="ecb88-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb88-113">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-113">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb88-114">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb88-114">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="ecb88-115">識別資源索引子的控制碼，以從中建立 PRI 資訊。</span><span class="sxs-lookup"><span data-stu-id="ecb88-115">A handle identifying the resource indexer from which to create the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="ecb88-116">*packagingMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-116">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb88-117">類型： **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb88-117">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="ecb88-118">指定 PRI 資訊是否應獨立，或為資源套件。</span><span class="sxs-lookup"><span data-stu-id="ecb88-118">Specifies whether the PRI info should be standalone, or be a resource pack.</span></span> <span data-ttu-id="ecb88-119">不支援 **MrmPackagingModeAutoSplit** 。</span><span class="sxs-lookup"><span data-stu-id="ecb88-119">**MrmPackagingModeAutoSplit** is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ecb88-120">*packagingOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-120">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb88-121">類型： **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb88-121">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="ecb88-122">指定 PRI 資訊的其他選項。</span><span class="sxs-lookup"><span data-stu-id="ecb88-122">Specifies additional options about the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="ecb88-123">*outputPriData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-123">*outputPriData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb88-124">類型：**位元組 \* \***</span><span class="sxs-lookup"><span data-stu-id="ecb88-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="ecb88-125">位元組指標的位址。</span><span class="sxs-lookup"><span data-stu-id="ecb88-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="ecb88-126">此函式會配置記憶體，並將指標傳回至 *outputPriData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="ecb88-126">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="ecb88-127">使用您的位元組指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) ，以釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="ecb88-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="ecb88-128">*outputPriSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-128">*outputPriSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb88-129">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="ecb88-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="ecb88-130">ULONG 的位址。</span><span class="sxs-lookup"><span data-stu-id="ecb88-130">The address of a ULONG.</span></span> <span data-ttu-id="ecb88-131">在 _outputPriSize \* 中，此函式會傳回 *outputPriData* 所指向之已配置記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="ecb88-131">In _outputPriSize\*, the function returns the size of the allocated memory pointed to by *outputPriData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb88-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecb88-132">Return value</span></span>

<span data-ttu-id="ecb88-133">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ecb88-133">Type: **HRESULT**</span></span>

<span data-ttu-id="ecb88-134">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="ecb88-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="ecb88-135">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="ecb88-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecb88-136">備註</span><span class="sxs-lookup"><span data-stu-id="ecb88-136">Remarks</span></span>

<span data-ttu-id="ecb88-137">如果您將 *outputPriData* 傳遞至 [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md)，則在您完成使用資源索引子之前，請勿釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="ecb88-137">If you pass *outputPriData* to [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), then don't free the memory until after you've finished using the resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb88-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecb88-138">Requirements</span></span>



| <span data-ttu-id="ecb88-139">需求</span><span class="sxs-lookup"><span data-stu-id="ecb88-139">Requirement</span></span> | <span data-ttu-id="ecb88-140">值</span><span class="sxs-lookup"><span data-stu-id="ecb88-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb88-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecb88-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb88-142">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ecb88-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecb88-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb88-144">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecb88-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ecb88-145">標頭</span><span class="sxs-lookup"><span data-stu-id="ecb88-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb88-146"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb88-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="ecb88-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="ecb88-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecb88-148"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecb88-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="ecb88-149">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb88-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecb88-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb88-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ecb88-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecb88-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb88-152">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="ecb88-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

