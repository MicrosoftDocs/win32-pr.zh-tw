---
title: IGatherNotify AddScope (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify AddScope (已淘汰的) 方法
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- AddScope (淘汰的) 方法舊版 Windows 環境功能
- AddScope (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能，AddScope (已淘汰的) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322180"
---
# <a name="igathernotifyaddscope-deprecated-method"></a><span data-ttu-id="74eec-107">IGatherNotify：： AddScope (已淘汰的) 方法</span><span class="sxs-lookup"><span data-stu-id="74eec-107">IGatherNotify::AddScope (Deprecated) method</span></span>

<span data-ttu-id="74eec-108">\[**AddScope** 可能會在作業系統或產品的後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="74eec-108">\[**AddScope** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="74eec-109">此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。</span><span class="sxs-lookup"><span data-stu-id="74eec-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="74eec-110">新增您要監視的起始頁或 URL。</span><span class="sxs-lookup"><span data-stu-id="74eec-110">Adds the start page or URL you are monitoring.</span></span> <span data-ttu-id="74eec-111">這會在您連接時起始增量編目，然後假設所有進一步的 URL 變更都是由通知所變更。</span><span class="sxs-lookup"><span data-stu-id="74eec-111">This initiates an incremental crawl when you connect, and then assumes all further URL changes are by notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="74eec-112">語法</span><span class="sxs-lookup"><span data-stu-id="74eec-112">Syntax</span></span>


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a><span data-ttu-id="74eec-113">參數</span><span class="sxs-lookup"><span data-stu-id="74eec-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74eec-114">*bstrScope* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74eec-114">*bstrScope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74eec-115">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="74eec-115">Type: **BSTR**</span></span>

<span data-ttu-id="74eec-116">字串，指定您要監視的起始頁或 URLthat。</span><span class="sxs-lookup"><span data-stu-id="74eec-116">A string that specifies the start page or URLthat you are monitoring.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74eec-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="74eec-117">Return value</span></span>

<span data-ttu-id="74eec-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="74eec-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74eec-119">備註</span><span class="sxs-lookup"><span data-stu-id="74eec-119">Remarks</span></span>

<span data-ttu-id="74eec-120">當連接到存放區時，呼叫這個方法會啟動增量編目。</span><span class="sxs-lookup"><span data-stu-id="74eec-120">Calling this method starts an incremental crawl when connected to the store.</span></span> <span data-ttu-id="74eec-121">之後，假設所有的 URL 變更都是在初始更新之後的通知。</span><span class="sxs-lookup"><span data-stu-id="74eec-121">Thereafter, it is assumed that all URL changes are by notification after the initial update.</span></span>

 

 
