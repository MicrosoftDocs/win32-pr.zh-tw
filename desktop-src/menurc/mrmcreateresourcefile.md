---
title: 'MrmCreateResourceFile 函式 (MrmResourceIndexer) '
description: 在指定的資料夾中，于磁片上建立一個名為 \ 0034; resources. pri \ 0034; ) 或檔案的 (PRI 檔案。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- MrmCreateResourceFile 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686298"
---
# <a name="mrmcreateresourcefile-function"></a><span data-ttu-id="0722b-105">MrmCreateResourceFile 函式</span><span class="sxs-lookup"><span data-stu-id="0722b-105">MrmCreateResourceFile function</span></span>

<span data-ttu-id="0722b-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="0722b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0722b-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="0722b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0722b-108">在指定的資料夾中，于磁片上建立名稱為 "resources. pri" ) 或檔案的 PRI 檔案 (。</span><span class="sxs-lookup"><span data-stu-id="0722b-108">Creates a PRI file (named "resources.pri"), or files, on disk in the specified folder.</span></span> <span data-ttu-id="0722b-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="0722b-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0722b-110">語法</span><span class="sxs-lookup"><span data-stu-id="0722b-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="0722b-111">參數</span><span class="sxs-lookup"><span data-stu-id="0722b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0722b-112">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0722b-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0722b-113">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="0722b-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="0722b-114">識別資源索引子的控制碼，以從中建立 PRI 檔案。</span><span class="sxs-lookup"><span data-stu-id="0722b-114">A handle identifying the resource indexer from which to create the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="0722b-115">*packagingMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0722b-115">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0722b-116">類型： **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="0722b-116">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="0722b-117">指定 PRI 檔案是否應獨立、依資源限定詞自動分割，或為資源套件。</span><span class="sxs-lookup"><span data-stu-id="0722b-117">Specifies whether the PRI file should be standalone, be automatically split by resource qualifier, or be a resource pack.</span></span>

</dd> <dt>

<span data-ttu-id="0722b-118">*packagingOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0722b-118">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0722b-119">類型： **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="0722b-119">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="0722b-120">指定 PRI 檔案的其他選項。</span><span class="sxs-lookup"><span data-stu-id="0722b-120">Specifies additional options about the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="0722b-121">*outputDirectory*</span><span class="sxs-lookup"><span data-stu-id="0722b-121">*outputDirectory*</span></span> 
</dt> <dd>

<span data-ttu-id="0722b-122">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="0722b-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="0722b-123">要在其中儲存 PRI 檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="0722b-123">A path to a folder in which to save the PRI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0722b-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="0722b-124">Return value</span></span>

<span data-ttu-id="0722b-125">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0722b-125">Type: **HRESULT**</span></span>

<span data-ttu-id="0722b-126">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="0722b-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="0722b-127">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="0722b-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0722b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0722b-128">Requirements</span></span>



| <span data-ttu-id="0722b-129">需求</span><span class="sxs-lookup"><span data-stu-id="0722b-129">Requirement</span></span> | <span data-ttu-id="0722b-130">值</span><span class="sxs-lookup"><span data-stu-id="0722b-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0722b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0722b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0722b-132">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0722b-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0722b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0722b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0722b-134">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0722b-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0722b-135">標頭</span><span class="sxs-lookup"><span data-stu-id="0722b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0722b-136"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="0722b-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="0722b-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="0722b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="0722b-138"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0722b-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="0722b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0722b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0722b-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0722b-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0722b-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0722b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0722b-142">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="0722b-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

