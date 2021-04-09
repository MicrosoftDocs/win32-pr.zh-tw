---
title: 'MrmCreateResourceIndexerFromPreviousSchemaFile 函式 (MrmResourceIndexer) '
description: 從先前呼叫 MrmDumpPriFile 所建立的架構檔案，建立資源索引子。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- MrmCreateResourceIndexerFromPreviousSchemaFile 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 304e0aebe75ac416623cb1ec1053a7b6ae504194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686296"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a><span data-ttu-id="0f0ff-105">MrmCreateResourceIndexerFromPreviousSchemaFile 函式</span><span class="sxs-lookup"><span data-stu-id="0f0ff-105">MrmCreateResourceIndexerFromPreviousSchemaFile function</span></span>

<span data-ttu-id="0f0ff-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0f0ff-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0f0ff-108">從先前呼叫 [**MrmDumpPriFile**](mrmdumpprifile.md)所建立的架構檔案，建立資源索引子。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-108">Creates a resource indexer from a schema file created with a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span> <span data-ttu-id="0f0ff-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0ff-110">語法</span><span class="sxs-lookup"><span data-stu-id="0f0ff-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="0f0ff-111">參數</span><span class="sxs-lookup"><span data-stu-id="0f0ff-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f0ff-112">*projectRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0ff-113">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="0f0ff-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="0f0ff-114">您將產生 PRI 檔案之 UWP 應用程式的專案根目錄。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="0f0ff-115">換句話說，是該應用程式資源檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="0f0ff-116">您可以指定此項，如此您就可以在對相同資源索引子的後續 API 呼叫中，指定相對於該根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="0f0ff-117">*platformVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0ff-118">類型： **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="0f0ff-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="0f0ff-119">資源索引子的目標平臺版本。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="0f0ff-120">*defaultQualifiers* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0ff-121">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="0f0ff-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="0f0ff-122">預設資源限定詞的清單。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="0f0ff-123">例如，L "language-en-us \_ scale-100 \_ 對比-標準"</span><span class="sxs-lookup"><span data-stu-id="0f0ff-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="0f0ff-124">*schemaFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-124">*schemaFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0ff-125">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="0f0ff-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="0f0ff-126">先前呼叫 [**MrmDumpPriFile**](mrmdumpprifile.md)所建立之架構檔案的完整檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-126">A full file path to a schema file created by a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f0ff-127">*索引子* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0ff-128">類型： \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="0f0ff-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="0f0ff-129">資源索引子控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f0ff-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f0ff-130">Return value</span></span>

<span data-ttu-id="0f0ff-131">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0f0ff-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0f0ff-132">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="0f0ff-133">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="0f0ff-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f0ff-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f0ff-134">Requirements</span></span>



| <span data-ttu-id="0f0ff-135">需求</span><span class="sxs-lookup"><span data-stu-id="0f0ff-135">Requirement</span></span> | <span data-ttu-id="0f0ff-136">值</span><span class="sxs-lookup"><span data-stu-id="0f0ff-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0ff-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f0ff-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0f0ff-138">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0f0ff-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f0ff-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0f0ff-140">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f0ff-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0f0ff-141">標頭</span><span class="sxs-lookup"><span data-stu-id="0f0ff-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f0ff-142"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f0ff-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="0f0ff-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f0ff-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f0ff-144"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f0ff-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="0f0ff-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0f0ff-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f0ff-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f0ff-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0f0ff-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f0ff-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0ff-148">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="0f0ff-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

