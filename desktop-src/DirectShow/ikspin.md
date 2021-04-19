---
description: IKsPin 介面會提供方法，以在核心模式篩選器上取出 pin 所支援的媒體。 除了此處所示的 IKsPin 之外，還有其他方法，但不支援 DirectShow。
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: 'IKsPin 介面 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967009"
---
# <a name="ikspin-interface"></a><span data-ttu-id="091e6-104">IKsPin 介面</span><span class="sxs-lookup"><span data-stu-id="091e6-104">IKsPin interface</span></span>

<span data-ttu-id="091e6-105">`IKsPin`介面會提供方法，以在核心模式篩選器上取得 pin 所支援的媒體。</span><span class="sxs-lookup"><span data-stu-id="091e6-105">The `IKsPin` interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter.</span></span> <span data-ttu-id="091e6-106">`IKsPin` 除了此處所示的以外，還有其他方法，但不支援 DirectShow。</span><span class="sxs-lookup"><span data-stu-id="091e6-106">`IKsPin` has additional methods besides the one shown here, but they are not supported for DirectShow.</span></span>

## <a name="members"></a><span data-ttu-id="091e6-107">成員</span><span class="sxs-lookup"><span data-stu-id="091e6-107">Members</span></span>

<span data-ttu-id="091e6-108">**IKsPin** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="091e6-108">The **IKsPin** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="091e6-109">**IKsPin** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="091e6-109">**IKsPin** also has these types of members:</span></span>

-   [<span data-ttu-id="091e6-110">方法</span><span class="sxs-lookup"><span data-stu-id="091e6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="091e6-111">方法</span><span class="sxs-lookup"><span data-stu-id="091e6-111">Methods</span></span>

<span data-ttu-id="091e6-112">**IKsPin** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="091e6-112">The **IKsPin** interface has these methods.</span></span>



| <span data-ttu-id="091e6-113">方法</span><span class="sxs-lookup"><span data-stu-id="091e6-113">Method</span></span>                                          | <span data-ttu-id="091e6-114">描述</span><span class="sxs-lookup"><span data-stu-id="091e6-114">Description</span></span>                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="091e6-115">**KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="091e6-115">**KsQueryMediums**</span></span>](ikspin-ksquerymediums.md) | <span data-ttu-id="091e6-116">抓取 pin 所支援的媒體。</span><span class="sxs-lookup"><span data-stu-id="091e6-116">Retrieves the mediums supported by a pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="091e6-117">備註</span><span class="sxs-lookup"><span data-stu-id="091e6-117">Remarks</span></span>

<span data-ttu-id="091e6-118">您必須在 Ksproxy 之前包含 Ks。</span><span class="sxs-lookup"><span data-stu-id="091e6-118">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="091e6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="091e6-119">Requirements</span></span>



| <span data-ttu-id="091e6-120">需求</span><span class="sxs-lookup"><span data-stu-id="091e6-120">Requirement</span></span> | <span data-ttu-id="091e6-121">值</span><span class="sxs-lookup"><span data-stu-id="091e6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="091e6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="091e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="091e6-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="091e6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="091e6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="091e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="091e6-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="091e6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="091e6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="091e6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="091e6-127"><dt>Ksproxy。h</dt></span><span class="sxs-lookup"><span data-stu-id="091e6-127"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="091e6-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="091e6-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="091e6-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="091e6-129"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
