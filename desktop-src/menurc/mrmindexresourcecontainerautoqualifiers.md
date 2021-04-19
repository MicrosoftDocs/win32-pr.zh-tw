---
title: 'MrmIndexResourceContainerAutoQualifiers 函式 (MrmResourceIndexer) '
description: 為屬於 UWP 應用程式的 .resw/resources.resjson) 或 priinfo 或 prifile 資源 ( 檔內包含的字串資源編制索引。
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- MrmIndexResourceContainerAutoQualifiers 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967561"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a><span data-ttu-id="6bcd9-104">MrmIndexResourceContainerAutoQualifiers 函式</span><span class="sxs-lookup"><span data-stu-id="6bcd9-104">MrmIndexResourceContainerAutoQualifiers function</span></span>

<span data-ttu-id="6bcd9-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6bcd9-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="6bcd9-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6bcd9-107">為屬於 UWP 應用程式的 .resw/resources.resjson) 或 priinfo 或 prifile 資源 ( 檔內包含的字串資源編制索引。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-107">Indexes the string resources contained inside a Resources File (.resw/.resjson), or a .priinfo or .prifile, belonging to a UWP app.</span></span> <span data-ttu-id="6bcd9-108">從 *containerPath* 參數推斷資源限定詞的清單。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-108">Infers a list of resource qualifiers from the *containerPath* parameter.</span></span> <span data-ttu-id="6bcd9-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="6bcd9-110">語法</span><span class="sxs-lookup"><span data-stu-id="6bcd9-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a><span data-ttu-id="6bcd9-111">參數</span><span class="sxs-lookup"><span data-stu-id="6bcd9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bcd9-112">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bcd9-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bcd9-113">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="6bcd9-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="6bcd9-114">識別將為字串資源編制索引之資源索引子的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="6bcd9-115">*containerPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bcd9-115">*containerPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bcd9-116">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6bcd9-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="6bcd9-117">.Resw、. resources.resjson、. priinfo 或. prifile 的相對路徑，其中包含您想要編制索引的字串資源。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-117">A relative path to a .resw, .resjson, .priinfo, or .prifile containing string resources that you want to index.</span></span> <span data-ttu-id="6bcd9-118">此路徑相對於您要產生 PRI 檔案之 UWP 應用程式的專案根目錄。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-118">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="6bcd9-119">該專案根目錄是您傳遞至 [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)的 *projectRoot* 值。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-119">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bcd9-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bcd9-120">Return value</span></span>

<span data-ttu-id="6bcd9-121">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6bcd9-121">Type: **HRESULT**</span></span>

<span data-ttu-id="6bcd9-122">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-122">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="6bcd9-123">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-123">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bcd9-124">備註</span><span class="sxs-lookup"><span data-stu-id="6bcd9-124">Remarks</span></span>

<span data-ttu-id="6bcd9-125">系統會從 *containerPath* 推斷資源限定詞。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-125">Resource qualifiers are inferred from *containerPath*.</span></span> <span data-ttu-id="6bcd9-126">例如，值為 L "en-us \\ \\ resources. .resw" 會新增具有限定詞 "language-en-us" 的字串資源。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-126">For example, a value of L"en-US\\\\resources.resw" adds string resources with the qualifier "language-en-US".</span></span>

<span data-ttu-id="6bcd9-127">當您稍後從此資源索引子產生 PRI 檔案時，資源檔的名稱將會用來做為這些資源的資源對應子樹名稱。</span><span class="sxs-lookup"><span data-stu-id="6bcd9-127">The name of the Resources File will be used as the resource map subtree name for these resources when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bcd9-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bcd9-128">Requirements</span></span>



| <span data-ttu-id="6bcd9-129">需求</span><span class="sxs-lookup"><span data-stu-id="6bcd9-129">Requirement</span></span> | <span data-ttu-id="6bcd9-130">值</span><span class="sxs-lookup"><span data-stu-id="6bcd9-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcd9-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bcd9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6bcd9-132">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bcd9-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6bcd9-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bcd9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6bcd9-134">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bcd9-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6bcd9-135">標頭</span><span class="sxs-lookup"><span data-stu-id="6bcd9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bcd9-136"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bcd9-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="6bcd9-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="6bcd9-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bcd9-138"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bcd9-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="6bcd9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6bcd9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bcd9-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bcd9-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6bcd9-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bcd9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bcd9-142">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="6bcd9-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

