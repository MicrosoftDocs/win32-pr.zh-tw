---
title: 'MrmFreeMemory 函式 (MrmResourceIndexer) '
description: 釋放 MrmCreateConfigInMemory、MrmCreateResourceFileInMemory、MrmDumpPriFileInMemory 和 MrmDumpPriDataInMemory 所配置的記憶體。
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- MrmFreeMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965109"
---
# <a name="mrmfreememory-function"></a><span data-ttu-id="7f65d-104">MrmFreeMemory 函式</span><span class="sxs-lookup"><span data-stu-id="7f65d-104">MrmFreeMemory function</span></span>

<span data-ttu-id="7f65d-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="7f65d-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7f65d-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="7f65d-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7f65d-107">釋放 [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md)、 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)、 [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)和 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7f65d-107">Frees memory allocated by [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), and [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="7f65d-108">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="7f65d-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f65d-109">語法</span><span class="sxs-lookup"><span data-stu-id="7f65d-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a><span data-ttu-id="7f65d-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f65d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f65d-111">*資料* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f65d-111">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f65d-112">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="7f65d-112">Type: \**BYTE\** _</span></span>

<span data-ttu-id="7f65d-113">由 [_ *MrmCreateConfigInMemory* \*](mrmcreateconfiginmemory.md)、 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)、 [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)或 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)所配置和傳回之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="7f65d-113">A pointer to memory allocated and returned by [_ *MrmCreateConfigInMemory*\*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f65d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f65d-114">Return value</span></span>

<span data-ttu-id="7f65d-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f65d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="7f65d-116">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="7f65d-116">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="7f65d-117">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="7f65d-117">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f65d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f65d-118">Requirements</span></span>



| <span data-ttu-id="7f65d-119">需求</span><span class="sxs-lookup"><span data-stu-id="7f65d-119">Requirement</span></span> | <span data-ttu-id="7f65d-120">值</span><span class="sxs-lookup"><span data-stu-id="7f65d-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f65d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f65d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f65d-122">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f65d-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7f65d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f65d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f65d-124">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f65d-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f65d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7f65d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f65d-126"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f65d-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="7f65d-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f65d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f65d-128"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f65d-128"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="7f65d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7f65d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f65d-130"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f65d-130"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7f65d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f65d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f65d-132">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="7f65d-132">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

