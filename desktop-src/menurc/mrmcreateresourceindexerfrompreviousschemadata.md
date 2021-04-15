---
title: 'MrmCreateResourceIndexerFromPreviousSchemaData 函式 (MrmResourceIndexer) '
description: 從先前對 MrmDumpPriFileInMemory 或 MrmDumpPriDataInMemory 的呼叫所建立的記憶體內部架構資料，建立資源索引子。
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- MrmCreateResourceIndexerFromPreviousSchemaData 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465600"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a><span data-ttu-id="96bad-104">MrmCreateResourceIndexerFromPreviousSchemaData 函式</span><span class="sxs-lookup"><span data-stu-id="96bad-104">MrmCreateResourceIndexerFromPreviousSchemaData function</span></span>

<span data-ttu-id="96bad-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="96bad-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="96bad-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="96bad-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="96bad-107">從先前對 [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) 或 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)的呼叫所建立的記憶體內部架構資料，建立資源索引子。</span><span class="sxs-lookup"><span data-stu-id="96bad-107">Creates a resource indexer from in-memory schema data created with a previous call to either [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="96bad-108">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="96bad-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="96bad-109">語法</span><span class="sxs-lookup"><span data-stu-id="96bad-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="96bad-110">參數</span><span class="sxs-lookup"><span data-stu-id="96bad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96bad-111">*projectRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96bad-111">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96bad-112">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="96bad-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="96bad-113">您將產生 PRI 檔案之 UWP 應用程式的專案根目錄。</span><span class="sxs-lookup"><span data-stu-id="96bad-113">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="96bad-114">換句話說，是該應用程式資源檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="96bad-114">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="96bad-115">您可以指定此項，如此您就可以在對相同資源索引子的後續 API 呼叫中，指定相對於該根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="96bad-115">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="96bad-116">*platformVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96bad-116">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96bad-117">類型： **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="96bad-117">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="96bad-118">資源索引子的目標平臺版本。</span><span class="sxs-lookup"><span data-stu-id="96bad-118">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="96bad-119">*defaultQualifiers* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="96bad-119">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="96bad-120">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="96bad-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="96bad-121">預設資源限定詞的清單。</span><span class="sxs-lookup"><span data-stu-id="96bad-121">A list of default resource qualifiers.</span></span> <span data-ttu-id="96bad-122">例如，L "language-en-us \_ scale-100 \_ 對比-標準"</span><span class="sxs-lookup"><span data-stu-id="96bad-122">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="96bad-123">*schemaXmlData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96bad-123">*schemaXmlData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96bad-124">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="96bad-124">Type: \**BYTE\** _</span></span>

<span data-ttu-id="96bad-125">先前呼叫 [_ *MrmDumpPriFileInMemory* \*](mrmdumpprifileinmemory.md)或 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)所建立之架構資料的指標。</span><span class="sxs-lookup"><span data-stu-id="96bad-125">A pointer to schema data created by a previous call to either [_ *MrmDumpPriFileInMemory*\*](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="96bad-126">在您完成使用此函數所建立的資源索引子之前，請勿釋放 *schemaXmlData* 。</span><span class="sxs-lookup"><span data-stu-id="96bad-126">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="96bad-127">*schemaXmlSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96bad-127">*schemaXmlSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96bad-128">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="96bad-128">Type: **ULONG**</span></span>

<span data-ttu-id="96bad-129">*SchemaXmlData* 所指向之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="96bad-129">The size of the data pointed to by *schemaXmlData*.</span></span>

</dd> <dt>

<span data-ttu-id="96bad-130">*索引子* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="96bad-130">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="96bad-131">類型： \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="96bad-131">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="96bad-132">資源索引子控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="96bad-132">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96bad-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="96bad-133">Return value</span></span>

<span data-ttu-id="96bad-134">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="96bad-134">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="96bad-135">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="96bad-135">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="96bad-136">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="96bad-136">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="96bad-137">備註</span><span class="sxs-lookup"><span data-stu-id="96bad-137">Remarks</span></span>

<span data-ttu-id="96bad-138">在您完成使用此函數所建立的資源索引子之前，請勿釋放 *schemaXmlData* 。</span><span class="sxs-lookup"><span data-stu-id="96bad-138">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="96bad-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="96bad-139">Requirements</span></span>



| <span data-ttu-id="96bad-140">需求</span><span class="sxs-lookup"><span data-stu-id="96bad-140">Requirement</span></span> | <span data-ttu-id="96bad-141">值</span><span class="sxs-lookup"><span data-stu-id="96bad-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96bad-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96bad-142">Minimum supported client</span></span><br/> | <span data-ttu-id="96bad-143">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96bad-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="96bad-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96bad-144">Minimum supported server</span></span><br/> | <span data-ttu-id="96bad-145">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96bad-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="96bad-146">標頭</span><span class="sxs-lookup"><span data-stu-id="96bad-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="96bad-147"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="96bad-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="96bad-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="96bad-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="96bad-149"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="96bad-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="96bad-150">DLL</span><span class="sxs-lookup"><span data-stu-id="96bad-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96bad-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96bad-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="96bad-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96bad-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96bad-153">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="96bad-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

