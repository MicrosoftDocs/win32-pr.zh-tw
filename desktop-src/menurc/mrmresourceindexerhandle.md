---
title: 'MrmResourceIndexerHandle 結構 (MrmResourceIndexer .h) '
description: 代表資源索引子物件的不透明控制碼。 控制碼由作業系統管理。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- MrmResourceIndexerHandle 結構功能表和其他資源
- PMrmResourceIndexerHandle 結構指標功能表和其他資源
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5786585597b5d23a6f6c0cd6842b655727c3ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385250"
---
# <a name="mrmresourceindexerhandle-structure"></a><span data-ttu-id="1374c-107">MrmResourceIndexerHandle 結構</span><span class="sxs-lookup"><span data-stu-id="1374c-107">MrmResourceIndexerHandle structure</span></span>

<span data-ttu-id="1374c-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="1374c-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1374c-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="1374c-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1374c-110">代表資源索引子物件的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="1374c-110">Represents an opaque handle to a resource indexer object.</span></span> <span data-ttu-id="1374c-111">控制碼由作業系統管理。</span><span class="sxs-lookup"><span data-stu-id="1374c-111">The handle is managed by the operating system.</span></span> <span data-ttu-id="1374c-112">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="1374c-112">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="1374c-113">語法</span><span class="sxs-lookup"><span data-stu-id="1374c-113">Syntax</span></span>


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a><span data-ttu-id="1374c-114">成員</span><span class="sxs-lookup"><span data-stu-id="1374c-114">Members</span></span>

<dl> <dt>

<span data-ttu-id="1374c-115">**處理**</span><span class="sxs-lookup"><span data-stu-id="1374c-115">**handle**</span></span>
</dt> <dd>

<span data-ttu-id="1374c-116">類型： **PVOID**</span><span class="sxs-lookup"><span data-stu-id="1374c-116">Type: **PVOID**</span></span>

</dd> <dd>

<span data-ttu-id="1374c-117">資源索引子物件的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="1374c-117">An opaque handle to a resource indexer object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1374c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1374c-118">Requirements</span></span>



| <span data-ttu-id="1374c-119">需求</span><span class="sxs-lookup"><span data-stu-id="1374c-119">Requirement</span></span> | <span data-ttu-id="1374c-120">值</span><span class="sxs-lookup"><span data-stu-id="1374c-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1374c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1374c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1374c-122">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1374c-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1374c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1374c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1374c-124">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1374c-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1374c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1374c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1374c-126"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="1374c-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1374c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1374c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1374c-128">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="1374c-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

