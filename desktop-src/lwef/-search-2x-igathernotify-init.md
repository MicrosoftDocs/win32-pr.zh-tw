---
title: IGatherNotify Init (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify Init (已淘汰的) 方法
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Init (淘汰的) 方法舊版 Windows 環境功能
- Init (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能、Init (已淘汰的) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992268"
---
# <a name="igathernotifyinit-deprecated-method"></a><span data-ttu-id="33de8-107">IGatherNotify：： Init (已淘汰的) 方法</span><span class="sxs-lookup"><span data-stu-id="33de8-107">IGatherNotify::Init (Deprecated) method</span></span>

<span data-ttu-id="33de8-108">\[**Init** 可能會在作業系統或產品的後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="33de8-108">\[**Init** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="33de8-109">此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。</span><span class="sxs-lookup"><span data-stu-id="33de8-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="33de8-110">初始化收集介面。</span><span class="sxs-lookup"><span data-stu-id="33de8-110">Initializes the Gatherer interface.</span></span> <span data-ttu-id="33de8-111">也會指定要通知的索引，以及要監視的應用程式存放區。</span><span class="sxs-lookup"><span data-stu-id="33de8-111">Also specifies the index to notify and the application store to monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="33de8-112">語法</span><span class="sxs-lookup"><span data-stu-id="33de8-112">Syntax</span></span>


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a><span data-ttu-id="33de8-113">參數</span><span class="sxs-lookup"><span data-stu-id="33de8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33de8-114">*bstrApplication* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33de8-114">*bstrApplication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33de8-115">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="33de8-115">Type: **BSTR**</span></span>

<span data-ttu-id="33de8-116">指定目標應用程式的字串。</span><span class="sxs-lookup"><span data-stu-id="33de8-116">A string that specifies the target application.</span></span>

</dd> <dt>

<span data-ttu-id="33de8-117">*bstrProject* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33de8-117">*bstrProject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33de8-118">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="33de8-118">Type: **BSTR**</span></span>

<span data-ttu-id="33de8-119">字串，指定要傳遞收集程式資訊的索引子名稱。</span><span class="sxs-lookup"><span data-stu-id="33de8-119">A string that specifies the name of the indexer to pass gatherer information to.</span></span>

</dd> <dt>

<span data-ttu-id="33de8-120">*varScopesBstrArray* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33de8-120">*varScopesBstrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33de8-121">類型： **variant**</span><span class="sxs-lookup"><span data-stu-id="33de8-121">Type: **variant**</span></span>

<span data-ttu-id="33de8-122">選擇性參數，可讓您傳遞要初始化的範圍陣列。</span><span class="sxs-lookup"><span data-stu-id="33de8-122">Optional parameter, that enables you to pass an array of scopes to be initialized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33de8-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="33de8-123">Return value</span></span>

<span data-ttu-id="33de8-124">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33de8-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33de8-125">備註</span><span class="sxs-lookup"><span data-stu-id="33de8-125">Remarks</span></span>

<span data-ttu-id="33de8-126">使用 application = "RSApp"，Project = "MyIndex" 初始化。</span><span class="sxs-lookup"><span data-stu-id="33de8-126">Initialize with application="RSApp", Project="MyIndex".</span></span>

 

 
