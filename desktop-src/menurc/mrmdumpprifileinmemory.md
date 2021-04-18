---
title: 'MrmDumpPriFileInMemory 函式 (MrmResourceIndexer) '
description: 傾印 PRI 檔案 (這是其 XML 對等 (的二進位) ，如同記憶體中的資料) ，以便更容易閱讀。
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- MrmDumpPriFileInMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965062"
---
# <a name="mrmdumpprifileinmemory-function"></a><span data-ttu-id="bfde8-104">MrmDumpPriFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="bfde8-104">MrmDumpPriFileInMemory function</span></span>

<span data-ttu-id="bfde8-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bfde8-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bfde8-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bfde8-107">傾印 PRI 檔案 (這是其 XML 對等 (的二進位) ，如同記憶體中的資料) ，以便更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="bfde8-107">Dumps a PRI file (which is binary) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="bfde8-108">此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="bfde8-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="bfde8-109">使用相同的指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) 來釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="bfde8-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="bfde8-110">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="bfde8-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfde8-111">語法</span><span class="sxs-lookup"><span data-stu-id="bfde8-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="bfde8-112">參數</span><span class="sxs-lookup"><span data-stu-id="bfde8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfde8-113">*indexFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-113">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde8-114">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bfde8-114">Type: **PCWSTR**</span></span>

<span data-ttu-id="bfde8-115">PRI 檔案的完整檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="bfde8-115">A full file path to a PRI file.</span></span> <span data-ttu-id="bfde8-116">這是將傾印至 XML 的 PRI 檔案。</span><span class="sxs-lookup"><span data-stu-id="bfde8-116">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="bfde8-117">*schemaPriFile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-117">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde8-118">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="bfde8-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="bfde8-119">架構檔案的選擇性完整檔案路徑， (或代表架構的 PRI 檔案;請參閱備註) 。</span><span class="sxs-lookup"><span data-stu-id="bfde8-119">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="bfde8-120">*dumpType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-120">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde8-121">類型： **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="bfde8-121">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="bfde8-122">指定 XML 傾印的詳細程度，或是否應該傾印架構。</span><span class="sxs-lookup"><span data-stu-id="bfde8-122">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="bfde8-123">*outputXmlData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-123">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde8-124">類型：**位元組 \* \***</span><span class="sxs-lookup"><span data-stu-id="bfde8-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="bfde8-125">位元組指標的位址。</span><span class="sxs-lookup"><span data-stu-id="bfde8-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="bfde8-126">此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="bfde8-126">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="bfde8-127">使用您的位元組指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) ，以釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="bfde8-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="bfde8-128">*outputXmlSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-128">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde8-129">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="bfde8-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="bfde8-130">ULONG 的位址。</span><span class="sxs-lookup"><span data-stu-id="bfde8-130">The address of a ULONG.</span></span> <span data-ttu-id="bfde8-131">在 _outputXmlSize \* 中，此函式會傳回 *outputXmlData* 所指向之已配置記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="bfde8-131">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfde8-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfde8-132">Return value</span></span>

<span data-ttu-id="bfde8-133">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfde8-133">Type: **HRESULT**</span></span>

<span data-ttu-id="bfde8-134">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="bfde8-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="bfde8-135">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="bfde8-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfde8-136">備註</span><span class="sxs-lookup"><span data-stu-id="bfde8-136">Remarks</span></span>

<span data-ttu-id="bfde8-137">無架構的資源套件是使用傳遞至 [**MrmCreateResourceFile**](mrmcreateresourcefile.md)或 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (的 [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md)引數，或在 PRI 設定檔) 中使用 *omitSchemaFromResourcePacks* 參數所建立的資源套件。</span><span class="sxs-lookup"><span data-stu-id="bfde8-137">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="bfde8-138">若要傾印無架構的資源套件，請將主要封裝 PRI 資料的路徑傳遞為 *schemaPriFile* 參數的引數。</span><span class="sxs-lookup"><span data-stu-id="bfde8-138">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfde8-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfde8-139">Requirements</span></span>



| <span data-ttu-id="bfde8-140">需求</span><span class="sxs-lookup"><span data-stu-id="bfde8-140">Requirement</span></span> | <span data-ttu-id="bfde8-141">值</span><span class="sxs-lookup"><span data-stu-id="bfde8-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfde8-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfde8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="bfde8-143">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bfde8-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfde8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="bfde8-145">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfde8-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bfde8-146">標頭</span><span class="sxs-lookup"><span data-stu-id="bfde8-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfde8-147"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="bfde8-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="bfde8-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="bfde8-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="bfde8-149"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfde8-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="bfde8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="bfde8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfde8-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfde8-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bfde8-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfde8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfde8-153">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="bfde8-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

