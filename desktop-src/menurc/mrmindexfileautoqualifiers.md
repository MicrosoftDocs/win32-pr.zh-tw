---
title: 'MrmIndexFileAutoQualifiers 函式 (MrmResourceIndexer) '
description: 編制屬於 UWP 應用程式的資源檔索引。 從 filePath 參數推斷資源限定詞的清單。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- MrmIndexFileAutoQualifiers 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093940"
---
# <a name="mrmindexfileautoqualifiers-function"></a><span data-ttu-id="7f2ad-106">MrmIndexFileAutoQualifiers 函式</span><span class="sxs-lookup"><span data-stu-id="7f2ad-106">MrmIndexFileAutoQualifiers function</span></span>

<span data-ttu-id="7f2ad-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7f2ad-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7f2ad-109">編制屬於 UWP 應用程式的資源檔索引。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="7f2ad-110">從 *filePath* 參數推斷資源限定詞的清單。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-110">Infers a list of resource qualifiers from the *filePath* parameter.</span></span> <span data-ttu-id="7f2ad-111">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2ad-112">語法</span><span class="sxs-lookup"><span data-stu-id="7f2ad-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a><span data-ttu-id="7f2ad-113">參數</span><span class="sxs-lookup"><span data-stu-id="7f2ad-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f2ad-114">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2ad-115">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="7f2ad-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="7f2ad-116">識別將為資源檔編制索引之資源索引子的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="7f2ad-117">*filePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-117">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f2ad-118">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7f2ad-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="7f2ad-119">檔案的相對路徑，該檔案包含您想要編制索引的資源。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-119">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="7f2ad-120">此路徑相對於您要產生 PRI 檔案之 UWP 應用程式的專案根目錄。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-120">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="7f2ad-121">該專案根目錄是您傳遞至 [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)的 *projectRoot* 值。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-121">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f2ad-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f2ad-122">Return value</span></span>

<span data-ttu-id="7f2ad-123">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f2ad-123">Type: **HRESULT**</span></span>

<span data-ttu-id="7f2ad-124">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="7f2ad-125">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2ad-126">備註</span><span class="sxs-lookup"><span data-stu-id="7f2ad-126">Remarks</span></span>

<span data-ttu-id="7f2ad-127">檔案 *路徑* 的檔案名區段會用來做為資源名稱;和資源限定詞衍生自其路徑。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-127">The file name segment of *filePath* is used as the resource name; and resource qualifiers are derived from its path.</span></span> <span data-ttu-id="7f2ad-128">例如，如果您將 L "Images \\ de-de \\ scale-100 \\background.png" 傳遞至 *filePath* ，則資源索引子會新增名為 "background.png" 的資源，其資源限定詞為 "language-de-de" 和 "scale-100"。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-128">For example, if you pass L"Images\\de-DE\\scale-100\\background.png" to *filePath* then the resource indexer adds a resource named "background.png" with resource qualifiers "language-de-DE" and "scale-100".</span></span>

<span data-ttu-id="7f2ad-129">當您稍後從此資源索引子產生 PRI 檔案時，會使用 L "Files" 做為此資源的資源對應子樹名稱。</span><span class="sxs-lookup"><span data-stu-id="7f2ad-129">L"Files" will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2ad-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f2ad-130">Requirements</span></span>



| <span data-ttu-id="7f2ad-131">需求</span><span class="sxs-lookup"><span data-stu-id="7f2ad-131">Requirement</span></span> | <span data-ttu-id="7f2ad-132">值</span><span class="sxs-lookup"><span data-stu-id="7f2ad-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2ad-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f2ad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2ad-134">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-134">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7f2ad-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f2ad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2ad-136">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f2ad-136">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f2ad-137">標頭</span><span class="sxs-lookup"><span data-stu-id="7f2ad-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f2ad-138"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f2ad-138"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="7f2ad-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f2ad-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f2ad-140"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f2ad-140"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="7f2ad-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7f2ad-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f2ad-142"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f2ad-142"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7f2ad-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f2ad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2ad-144">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="7f2ad-144">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

