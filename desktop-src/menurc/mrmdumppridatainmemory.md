---
title: 'MrmDumpPriDataInMemory 函式 (MrmResourceIndexer) '
description: 傾印 PRI 資訊 (作為記憶體中的 blob，由先前對 MrmCreateResourceFileInMemory) 的呼叫所建立，以作為記憶體中資料) 的 XML 對等 (，以便更容易閱讀。
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- MrmDumpPriDataInMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966142"
---
# <a name="mrmdumppridatainmemory-function"></a><span data-ttu-id="d212c-104">MrmDumpPriDataInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="d212c-104">MrmDumpPriDataInMemory function</span></span>

<span data-ttu-id="d212c-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d212c-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d212c-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d212c-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d212c-107">傾印 PRI 資訊 (作為記憶體中的 blob，由先前對 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) 的呼叫所建立，以作為記憶體中資料) 的 XML 對等 (，以便更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="d212c-107">Dumps PRI info (as a blob in memory, created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="d212c-108">此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d212c-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="d212c-109">使用相同的指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) 來釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d212c-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="d212c-110">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="d212c-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="d212c-111">語法</span><span class="sxs-lookup"><span data-stu-id="d212c-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="d212c-112">參數</span><span class="sxs-lookup"><span data-stu-id="d212c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d212c-113">*inputPriData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d212c-113">*inputPriData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d212c-114">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="d212c-114">Type: \**BYTE\** _</span></span>

<span data-ttu-id="d212c-115">對 [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md)之前的呼叫所建立之 PRI 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="d212c-115">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d212c-116">*inputPriSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d212c-116">*inputPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d212c-117">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="d212c-117">Type: **ULONG**</span></span>

<span data-ttu-id="d212c-118">*InputPriData* 所指向之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="d212c-118">The size of the data pointed to by *inputPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="d212c-119">*schemaPriData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d212c-119">*schemaPriData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d212c-120">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="d212c-120">Type: \**BYTE\** _</span></span>

<span data-ttu-id="d212c-121">PRI 資訊的選擇性指標 (作為記憶體中的 blob) 代表前一次呼叫 [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md)所建立的架構資料。</span><span class="sxs-lookup"><span data-stu-id="d212c-121">An optional pointer to PRI info (as a blob in memory) representing schema data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="d212c-122">在您完成使用資源索引子之前，請勿釋放 *schemaPriData* 。</span><span class="sxs-lookup"><span data-stu-id="d212c-122">Don't free *schemaPriData* until after you've finished using the resource indexer.</span></span> <span data-ttu-id="d212c-123">另請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d212c-123">Also see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d212c-124">*schemaPriSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d212c-124">*schemaPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d212c-125">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="d212c-125">Type: **ULONG**</span></span>

<span data-ttu-id="d212c-126">*SchemaPriData* 所指向之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="d212c-126">The size of the data pointed to by *schemaPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="d212c-127">*dumpType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d212c-127">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d212c-128">類型： **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="d212c-128">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="d212c-129">指定 XML 傾印的詳細程度，或是否應該傾印架構。</span><span class="sxs-lookup"><span data-stu-id="d212c-129">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="d212c-130">*outputXmlData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d212c-130">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d212c-131">類型：**位元組 \* \***</span><span class="sxs-lookup"><span data-stu-id="d212c-131">Type: **BYTE\*\***</span></span>

<span data-ttu-id="d212c-132">位元組指標的位址。</span><span class="sxs-lookup"><span data-stu-id="d212c-132">The address of a pointer to BYTE.</span></span> <span data-ttu-id="d212c-133">此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d212c-133">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="d212c-134">使用您的位元組指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) ，以釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d212c-134">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="d212c-135">*outputXmlSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d212c-135">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d212c-136">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="d212c-136">Type: \**ULONG\** _</span></span>

<span data-ttu-id="d212c-137">ULONG 的位址。</span><span class="sxs-lookup"><span data-stu-id="d212c-137">The address of a ULONG.</span></span> <span data-ttu-id="d212c-138">在 _outputXmlSize \* 中，此函式會傳回 *outputXmlData* 所指向之已配置記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="d212c-138">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d212c-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="d212c-139">Return value</span></span>

<span data-ttu-id="d212c-140">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d212c-140">Type: **HRESULT**</span></span>

<span data-ttu-id="d212c-141">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="d212c-141">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="d212c-142">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="d212c-142">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d212c-143">備註</span><span class="sxs-lookup"><span data-stu-id="d212c-143">Remarks</span></span>

<span data-ttu-id="d212c-144">無架構的資源套件是使用傳遞至 [**MrmCreateResourceFile**](mrmcreateresourcefile.md)或 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (的 [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md)引數，或在 PRI 設定檔) 中使用 *omitSchemaFromResourcePacks* 參數所建立的資源套件。</span><span class="sxs-lookup"><span data-stu-id="d212c-144">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="d212c-145">若要傾印無架構的資源套件，請將主要封裝 PRI 資料的路徑傳遞為 *schemaPriData* 參數的引數。</span><span class="sxs-lookup"><span data-stu-id="d212c-145">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriData* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d212c-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="d212c-146">Requirements</span></span>



| <span data-ttu-id="d212c-147">需求</span><span class="sxs-lookup"><span data-stu-id="d212c-147">Requirement</span></span> | <span data-ttu-id="d212c-148">值</span><span class="sxs-lookup"><span data-stu-id="d212c-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d212c-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d212c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d212c-150">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d212c-150">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d212c-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d212c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d212c-152">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d212c-152">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d212c-153">標頭</span><span class="sxs-lookup"><span data-stu-id="d212c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="d212c-154"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="d212c-154"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="d212c-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="d212c-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="d212c-156"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d212c-156"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="d212c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="d212c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d212c-158"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d212c-158"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d212c-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d212c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d212c-160">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="d212c-160">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

