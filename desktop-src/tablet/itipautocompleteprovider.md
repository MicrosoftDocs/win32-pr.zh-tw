---
description: 管理文字輸入面板自動完成整合的應用程式端。
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: 'ITipAutocompleteProvider 介面 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997989"
---
# <a name="itipautocompleteprovider-interface"></a><span data-ttu-id="35f86-103">ITipAutocompleteProvider 介面</span><span class="sxs-lookup"><span data-stu-id="35f86-103">ITipAutocompleteProvider interface</span></span>

<span data-ttu-id="35f86-104">管理文字輸入面板自動完成整合的應用程式端。</span><span class="sxs-lookup"><span data-stu-id="35f86-104">Manages the application's side of the Text Input Panel auto complete integration.</span></span>

## <a name="members"></a><span data-ttu-id="35f86-105">成員</span><span class="sxs-lookup"><span data-stu-id="35f86-105">Members</span></span>

<span data-ttu-id="35f86-106">**ITipAutocompleteProvider** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="35f86-106">The **ITipAutocompleteProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="35f86-107">**ITipAutocompleteProvider** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35f86-107">**ITipAutocompleteProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="35f86-108">方法</span><span class="sxs-lookup"><span data-stu-id="35f86-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="35f86-109">方法</span><span class="sxs-lookup"><span data-stu-id="35f86-109">Methods</span></span>

<span data-ttu-id="35f86-110">**ITipAutocompleteProvider** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="35f86-110">The **ITipAutocompleteProvider** interface has these methods.</span></span>



| <span data-ttu-id="35f86-111">方法</span><span class="sxs-lookup"><span data-stu-id="35f86-111">Method</span></span>                                                                  | <span data-ttu-id="35f86-112">描述</span><span class="sxs-lookup"><span data-stu-id="35f86-112">Description</span></span>                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35f86-113">**顯示**</span><span class="sxs-lookup"><span data-stu-id="35f86-113">**Show**</span></span>](itipautocompleteprovider-show.md)                           | <span data-ttu-id="35f86-114">顯示或隱藏自動完成清單。</span><span class="sxs-lookup"><span data-stu-id="35f86-114">Displays or hides the auto complete list.</span></span><br/>                                                                 |
| [<span data-ttu-id="35f86-115">**UpdatePendingText**</span><span class="sxs-lookup"><span data-stu-id="35f86-115">**UpdatePendingText**</span></span>](itipautocompleteprovider-updatependingtext.md) | <span data-ttu-id="35f86-116">由自動完成用戶端用來通知應用程式使用者已筆跡輸入面板中的文字。</span><span class="sxs-lookup"><span data-stu-id="35f86-116">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="35f86-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="35f86-117">Requirements</span></span>



| <span data-ttu-id="35f86-118">需求</span><span class="sxs-lookup"><span data-stu-id="35f86-118">Requirement</span></span> | <span data-ttu-id="35f86-119">值</span><span class="sxs-lookup"><span data-stu-id="35f86-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35f86-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35f86-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35f86-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35f86-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="35f86-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35f86-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35f86-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="35f86-123">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="35f86-124">標頭</span><span class="sxs-lookup"><span data-stu-id="35f86-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="35f86-125"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="35f86-125"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="35f86-126">DLL</span><span class="sxs-lookup"><span data-stu-id="35f86-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f86-127"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f86-127"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="35f86-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35f86-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f86-129">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="35f86-129">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> <dt>

[<span data-ttu-id="35f86-130">**ITipAutocompleteClient 介面**</span><span class="sxs-lookup"><span data-stu-id="35f86-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> </dl>

 

