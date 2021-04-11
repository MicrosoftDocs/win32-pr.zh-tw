---
title: 'MrmCreateResourceIndexer 函式 (MrmResourceIndexer) '
description: 建立資源索引子，用來為 UWP 應用程式 (PRI) 檔產生封裝資源索引。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- MrmCreateResourceIndexer 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385122"
---
# <a name="mrmcreateresourceindexer-function"></a><span data-ttu-id="836db-105">MrmCreateResourceIndexer 函式</span><span class="sxs-lookup"><span data-stu-id="836db-105">MrmCreateResourceIndexer function</span></span>

<span data-ttu-id="836db-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="836db-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="836db-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="836db-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="836db-108">建立資源索引子，用來為 UWP 應用程式 (PRI) 檔產生封裝資源索引。</span><span class="sxs-lookup"><span data-stu-id="836db-108">Creates a resource indexer, used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="836db-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="836db-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="836db-110">語法</span><span class="sxs-lookup"><span data-stu-id="836db-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="836db-111">參數</span><span class="sxs-lookup"><span data-stu-id="836db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="836db-112">*packageFamilyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="836db-112">*packageFamilyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836db-113">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="836db-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="836db-114">您將產生 PRI 檔案之 UWP 應用程式的套件系列名稱。</span><span class="sxs-lookup"><span data-stu-id="836db-114">The package family name of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="836db-115">當您稍後從此資源索引子產生 PRI 檔案時，將會使用此值做為資源對應名稱。</span><span class="sxs-lookup"><span data-stu-id="836db-115">This value will be used as the resource map name when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="836db-116">*projectRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="836db-116">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836db-117">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="836db-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="836db-118">您將產生 PRI 檔案之 UWP 應用程式的專案根目錄。</span><span class="sxs-lookup"><span data-stu-id="836db-118">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="836db-119">換句話說，是該應用程式資源檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="836db-119">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="836db-120">您可以指定此項，如此您就可以在對相同資源索引子的後續 API 呼叫中，指定相對於該根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="836db-120">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="836db-121">*platformVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="836db-121">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836db-122">類型： **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="836db-122">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="836db-123">資源索引子的目標平臺版本。</span><span class="sxs-lookup"><span data-stu-id="836db-123">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="836db-124">*defaultQualifiers* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="836db-124">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="836db-125">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="836db-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="836db-126">預設資源限定詞的清單。</span><span class="sxs-lookup"><span data-stu-id="836db-126">A list of default resource qualifiers.</span></span> <span data-ttu-id="836db-127">例如，L "language-en-us \_ scale-100 \_ 對比-標準"</span><span class="sxs-lookup"><span data-stu-id="836db-127">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="836db-128">*索引子* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="836db-128">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="836db-129">類型： \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="836db-129">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="836db-130">資源索引子控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="836db-130">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="836db-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="836db-131">Return value</span></span>

<span data-ttu-id="836db-132">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="836db-132">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="836db-133">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="836db-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="836db-134">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="836db-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="836db-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="836db-135">Requirements</span></span>



| <span data-ttu-id="836db-136">需求</span><span class="sxs-lookup"><span data-stu-id="836db-136">Requirement</span></span> | <span data-ttu-id="836db-137">值</span><span class="sxs-lookup"><span data-stu-id="836db-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="836db-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="836db-138">Minimum supported client</span></span><br/> | <span data-ttu-id="836db-139">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="836db-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="836db-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="836db-140">Minimum supported server</span></span><br/> | <span data-ttu-id="836db-141">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="836db-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="836db-142">標頭</span><span class="sxs-lookup"><span data-stu-id="836db-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="836db-143"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="836db-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="836db-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="836db-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="836db-145"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="836db-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="836db-146">DLL</span><span class="sxs-lookup"><span data-stu-id="836db-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="836db-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="836db-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="836db-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="836db-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836db-149">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="836db-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

