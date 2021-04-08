---
title: 'MrmDumpPriFile 函式 (MrmResourceIndexer) '
description: 傾印 PRI 檔案 (這是其 XML 對等 (的二進位) ，以做為磁片) 上的檔案，以便更容易閱讀。
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- MrmDumpPriFile 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685989"
---
# <a name="mrmdumpprifile-function"></a><span data-ttu-id="d34fc-104">MrmDumpPriFile 函式</span><span class="sxs-lookup"><span data-stu-id="d34fc-104">MrmDumpPriFile function</span></span>

<span data-ttu-id="d34fc-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d34fc-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d34fc-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d34fc-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d34fc-107">傾印 PRI 檔案 (這是其 XML 對等 (的二進位) ，以做為磁片) 上的檔案，以便更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="d34fc-107">Dumps a PRI file (which is binary) to its XML equivalent (as a file on disk), in order to make it more easily readable.</span></span> <span data-ttu-id="d34fc-108">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="d34fc-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="d34fc-109">語法</span><span class="sxs-lookup"><span data-stu-id="d34fc-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="d34fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="d34fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34fc-111">*indexFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d34fc-111">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34fc-112">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d34fc-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="d34fc-113">PRI 檔案的完整檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="d34fc-113">A full file path to a PRI file.</span></span> <span data-ttu-id="d34fc-114">這是將傾印至 XML 的 PRI 檔案。</span><span class="sxs-lookup"><span data-stu-id="d34fc-114">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="d34fc-115">*schemaPriFile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d34fc-115">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d34fc-116">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d34fc-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="d34fc-117">架構檔案的選擇性完整檔案路徑， (或代表架構的 PRI 檔案;請參閱備註) 。</span><span class="sxs-lookup"><span data-stu-id="d34fc-117">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="d34fc-118">*dumpType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d34fc-118">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34fc-119">類型： **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="d34fc-119">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="d34fc-120">指定 XML 傾印的詳細程度，或是否應該傾印架構。</span><span class="sxs-lookup"><span data-stu-id="d34fc-120">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="d34fc-121">*outputXmlFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d34fc-121">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34fc-122">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d34fc-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="d34fc-123">要建立的 XML 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="d34fc-123">The path of an XML file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34fc-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="d34fc-124">Return value</span></span>

<span data-ttu-id="d34fc-125">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d34fc-125">Type: **HRESULT**</span></span>

<span data-ttu-id="d34fc-126">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="d34fc-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="d34fc-127">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="d34fc-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d34fc-128">備註</span><span class="sxs-lookup"><span data-stu-id="d34fc-128">Remarks</span></span>

<span data-ttu-id="d34fc-129">無架構的資源套件是使用傳遞至 [**MrmCreateResourceFile**](mrmcreateresourcefile.md)或 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (的 [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md)引數，或在 PRI 設定檔) 中使用 *omitSchemaFromResourcePacks* 參數所建立的資源套件。</span><span class="sxs-lookup"><span data-stu-id="d34fc-129">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="d34fc-130">若要傾印無架構的資源套件，請將主要封裝 PRI 資料的路徑傳遞為 *schemaPriFile* 參數的引數。</span><span class="sxs-lookup"><span data-stu-id="d34fc-130">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d34fc-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="d34fc-131">Requirements</span></span>



| <span data-ttu-id="d34fc-132">需求</span><span class="sxs-lookup"><span data-stu-id="d34fc-132">Requirement</span></span> | <span data-ttu-id="d34fc-133">值</span><span class="sxs-lookup"><span data-stu-id="d34fc-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d34fc-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d34fc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d34fc-135">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d34fc-135">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d34fc-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d34fc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d34fc-137">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d34fc-137">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d34fc-138">標頭</span><span class="sxs-lookup"><span data-stu-id="d34fc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d34fc-139"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="d34fc-139"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="d34fc-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="d34fc-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="d34fc-141"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d34fc-141"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="d34fc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d34fc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d34fc-143"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d34fc-143"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d34fc-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d34fc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34fc-145">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="d34fc-145">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

