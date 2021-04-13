---
title: 'MrmCreateConfigInMemory 函式 (MrmResourceIndexer) '
description: 建立新的初始化 PRI 設定資訊 (為記憶體內部資料，而不是檔案) 定義您指定的限定詞預設值。
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- MrmCreateConfigInMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509187"
---
# <a name="mrmcreateconfiginmemory-function"></a><span data-ttu-id="d1c36-104">MrmCreateConfigInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="d1c36-104">MrmCreateConfigInMemory function</span></span>

<span data-ttu-id="d1c36-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d1c36-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d1c36-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d1c36-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d1c36-107">建立新的初始化 PRI 設定資訊 (為記憶體內部資料，而不是檔案) 定義您指定的限定詞預設值。</span><span class="sxs-lookup"><span data-stu-id="d1c36-107">Creates new, initialized PRI configuration info (as in-memory data, not as a file) defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="d1c36-108">此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d1c36-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="d1c36-109">使用相同的指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) 來釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d1c36-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="d1c36-110">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="d1c36-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c36-111">語法</span><span class="sxs-lookup"><span data-stu-id="d1c36-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="d1c36-112">參數</span><span class="sxs-lookup"><span data-stu-id="d1c36-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c36-113">*platformVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1c36-113">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c36-114">類型： **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="d1c36-114">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="d1c36-115">平臺版本 (*targetOsVersion*) ，以用於產生的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="d1c36-115">The platform version (*targetOsVersion*) to use for the generated configuration info.</span></span>

</dd> <dt>

<span data-ttu-id="d1c36-116">*defaultQualifiers* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d1c36-116">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c36-117">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d1c36-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="d1c36-118">預設資源限定詞的清單。</span><span class="sxs-lookup"><span data-stu-id="d1c36-118">A list of default resource qualifiers.</span></span> <span data-ttu-id="d1c36-119">例如，L "language-en-us \_ scale-100 \_ 對比-標準"</span><span class="sxs-lookup"><span data-stu-id="d1c36-119">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="d1c36-120">*outputXmlData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1c36-120">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c36-121">類型：**位元組 \* \***</span><span class="sxs-lookup"><span data-stu-id="d1c36-121">Type: **BYTE\*\***</span></span>

<span data-ttu-id="d1c36-122">位元組指標的位址。</span><span class="sxs-lookup"><span data-stu-id="d1c36-122">The address of a pointer to BYTE.</span></span> <span data-ttu-id="d1c36-123">此函式會配置記憶體，並將指標傳回至 *outputXmlData* 中的該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d1c36-123">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="d1c36-124">使用您的位元組指標呼叫 [**MrmFreeMemory**](mrmfreememory.md) ，以釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d1c36-124">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="d1c36-125">*outputXmlSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1c36-125">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c36-126">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="d1c36-126">Type: \**ULONG\** _</span></span>

<span data-ttu-id="d1c36-127">ULONG 的位址。</span><span class="sxs-lookup"><span data-stu-id="d1c36-127">The address of a ULONG.</span></span> <span data-ttu-id="d1c36-128">在 _outputXmlSize \* 中，此函式會傳回 *outputXmlData* 所指向之已配置記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="d1c36-128">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c36-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1c36-129">Return value</span></span>

<span data-ttu-id="d1c36-130">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d1c36-130">Type: **HRESULT**</span></span>

<span data-ttu-id="d1c36-131">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="d1c36-131">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="d1c36-132">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="d1c36-132">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c36-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1c36-133">Requirements</span></span>



| <span data-ttu-id="d1c36-134">需求</span><span class="sxs-lookup"><span data-stu-id="d1c36-134">Requirement</span></span> | <span data-ttu-id="d1c36-135">值</span><span class="sxs-lookup"><span data-stu-id="d1c36-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c36-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1c36-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c36-137">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1c36-137">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d1c36-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1c36-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c36-139">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1c36-139">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1c36-140">標頭</span><span class="sxs-lookup"><span data-stu-id="d1c36-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1c36-141"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c36-141"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="d1c36-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1c36-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1c36-143"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1c36-143"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="d1c36-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c36-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c36-145"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c36-145"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d1c36-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1c36-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c36-147">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="d1c36-147">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

