---
title: 'MrmDestroyIndexerAndMessages 函式 (MrmResourceIndexer) '
description: 釋放與資源索引子相關聯的電腦資源。
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- MrmDestroyIndexerAndMessages 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e351c4d9e43bbb094d9738a6fef1b90c657b01e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025469"
---
# <a name="mrmdestroyindexerandmessages-function"></a><span data-ttu-id="b27a1-104">MrmDestroyIndexerAndMessages 函式</span><span class="sxs-lookup"><span data-stu-id="b27a1-104">MrmDestroyIndexerAndMessages function</span></span>

<span data-ttu-id="b27a1-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b27a1-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b27a1-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b27a1-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b27a1-107">釋放與資源索引子相關聯的電腦資源。</span><span class="sxs-lookup"><span data-stu-id="b27a1-107">Releases machine resources associated with a resource indexer.</span></span> <span data-ttu-id="b27a1-108">終結控制碼、釋出索引子，然後刪除任何訊息。</span><span class="sxs-lookup"><span data-stu-id="b27a1-108">Destroys the handle, frees the indexer, and deletes any messages.</span></span> <span data-ttu-id="b27a1-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="b27a1-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b27a1-110">語法</span><span class="sxs-lookup"><span data-stu-id="b27a1-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a><span data-ttu-id="b27a1-111">參數</span><span class="sxs-lookup"><span data-stu-id="b27a1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b27a1-112">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b27a1-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b27a1-113">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="b27a1-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="b27a1-114">識別要終結之資源索引子的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b27a1-114">A handle identifying the resource indexer to destroy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b27a1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b27a1-115">Return value</span></span>

<span data-ttu-id="b27a1-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b27a1-116">Type: **HRESULT**</span></span>

<span data-ttu-id="b27a1-117">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="b27a1-117">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="b27a1-118">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="b27a1-118">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b27a1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b27a1-119">Requirements</span></span>



| <span data-ttu-id="b27a1-120">需求</span><span class="sxs-lookup"><span data-stu-id="b27a1-120">Requirement</span></span> | <span data-ttu-id="b27a1-121">值</span><span class="sxs-lookup"><span data-stu-id="b27a1-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27a1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b27a1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b27a1-123">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b27a1-123">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b27a1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b27a1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b27a1-125">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b27a1-125">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b27a1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b27a1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b27a1-127"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="b27a1-127"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="b27a1-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="b27a1-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b27a1-129"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b27a1-129"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="b27a1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b27a1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b27a1-131"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b27a1-131"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b27a1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b27a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27a1-133">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="b27a1-133">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

