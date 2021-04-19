---
title: IGatherNotify OnDataChange (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify OnDataChange (已淘汰的) 方法
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange (淘汰的) 方法舊版 Windows 環境功能
- OnDataChange (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能，OnDataChange (已淘汰的) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988557"
---
# <a name="igathernotifyondatachange-deprecated-method"></a><span data-ttu-id="87c1b-107">IGatherNotify：： OnDataChange (已淘汰的) 方法</span><span class="sxs-lookup"><span data-stu-id="87c1b-107">IGatherNotify::OnDataChange (Deprecated) method</span></span>

<span data-ttu-id="87c1b-108">\[**OnDataChange** 可能會在作業系統或產品的後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="87c1b-108">\[**OnDataChange** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="87c1b-109">此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。</span><span class="sxs-lookup"><span data-stu-id="87c1b-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="87c1b-110">這個方法會通知索引子已變更的資料。</span><span class="sxs-lookup"><span data-stu-id="87c1b-110">This method notifies the indexer of data that has changed.</span></span> <span data-ttu-id="87c1b-111">當它將通知傳送至索引子時，它會包含變更類型、實體位址和邏輯位址。</span><span class="sxs-lookup"><span data-stu-id="87c1b-111">When it sends the notification to the indexer, it includes the type of change, physical address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c1b-112">語法</span><span class="sxs-lookup"><span data-stu-id="87c1b-112">Syntax</span></span>


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="87c1b-113">參數</span><span class="sxs-lookup"><span data-stu-id="87c1b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c1b-114">*eChangeAdvise* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87c1b-114">*eChangeAdvise* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c1b-115">類型： **long**</span><span class="sxs-lookup"><span data-stu-id="87c1b-115">Type: **long**</span></span>

<span data-ttu-id="87c1b-116">指定變更類型的列舉值。</span><span class="sxs-lookup"><span data-stu-id="87c1b-116">An enumerated value that specifies the type of change.</span></span>

</dd> <dt>

<span data-ttu-id="87c1b-117">*bstrPhysicalAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87c1b-117">*bstrPhysicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c1b-118">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="87c1b-118">Type: **BSTR**</span></span>

<span data-ttu-id="87c1b-119">變更之專案的實體位址。</span><span class="sxs-lookup"><span data-stu-id="87c1b-119">The physical address of the item that changed.</span></span>

</dd> <dt>

<span data-ttu-id="87c1b-120">*bstrLogicalAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87c1b-120">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c1b-121">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="87c1b-121">Type: **BSTR**</span></span>

<span data-ttu-id="87c1b-122">變更之專案的邏輯位址。</span><span class="sxs-lookup"><span data-stu-id="87c1b-122">The logical address of the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c1b-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="87c1b-123">Return value</span></span>

<span data-ttu-id="87c1b-124">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="87c1b-124">This method does not return a value.</span></span>

 

 
