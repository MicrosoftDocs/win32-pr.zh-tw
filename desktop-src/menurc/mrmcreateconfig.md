---
title: 'MrmCreateConfig 函式 (MrmResourceIndexer) '
description: 建立新的初始化 PRI 設定檔，以定義您指定的限定詞預設值。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- MrmCreateConfig 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965518"
---
# <a name="mrmcreateconfig-function"></a><span data-ttu-id="3cf15-105">MrmCreateConfig 函式</span><span class="sxs-lookup"><span data-stu-id="3cf15-105">MrmCreateConfig function</span></span>

<span data-ttu-id="3cf15-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="3cf15-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3cf15-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="3cf15-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3cf15-108">建立新的初始化 PRI 設定檔，以定義您指定的限定詞預設值。</span><span class="sxs-lookup"><span data-stu-id="3cf15-108">Creates a new, initialized PRI config file defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="3cf15-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="3cf15-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf15-110">語法</span><span class="sxs-lookup"><span data-stu-id="3cf15-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="3cf15-111">參數</span><span class="sxs-lookup"><span data-stu-id="3cf15-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf15-112">*platformVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cf15-112">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cf15-113">類型： **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="3cf15-113">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="3cf15-114">平臺版本 (*targetOsVersion*) 以用於產生的設定檔。</span><span class="sxs-lookup"><span data-stu-id="3cf15-114">The platform version (*targetOsVersion*) to use for the generated configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="3cf15-115">*defaultQualifiers* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3cf15-115">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cf15-116">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3cf15-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="3cf15-117">預設資源限定詞的清單。</span><span class="sxs-lookup"><span data-stu-id="3cf15-117">A list of default resource qualifiers.</span></span> <span data-ttu-id="3cf15-118">例如，L "language-en-us \_ scale-100 \_ 對比-標準"</span><span class="sxs-lookup"><span data-stu-id="3cf15-118">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="3cf15-119">*outputXmlFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cf15-119">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cf15-120">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3cf15-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="3cf15-121">要建立的設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="3cf15-121">The path of the configuration file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf15-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cf15-122">Return value</span></span>

<span data-ttu-id="3cf15-123">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3cf15-123">Type: **HRESULT**</span></span>

<span data-ttu-id="3cf15-124">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="3cf15-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="3cf15-125">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="3cf15-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf15-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cf15-126">Requirements</span></span>



| <span data-ttu-id="3cf15-127">需求</span><span class="sxs-lookup"><span data-stu-id="3cf15-127">Requirement</span></span> | <span data-ttu-id="3cf15-128">值</span><span class="sxs-lookup"><span data-stu-id="3cf15-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf15-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cf15-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf15-130">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf15-130">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3cf15-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cf15-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf15-132">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf15-132">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3cf15-133">標頭</span><span class="sxs-lookup"><span data-stu-id="3cf15-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf15-134"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf15-134"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="3cf15-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="3cf15-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3cf15-136"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cf15-136"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="3cf15-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3cf15-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cf15-138"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cf15-138"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3cf15-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cf15-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf15-140">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="3cf15-140">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

