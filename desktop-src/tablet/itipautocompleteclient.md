---
description: 可讓用戶端呼叫應用程式的文字輸入面板自動完成提供者物件。
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: 'ITipAutocompleteClient 介面 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980052"
---
# <a name="itipautocompleteclient-interface"></a><span data-ttu-id="5f383-103">ITipAutocompleteClient 介面</span><span class="sxs-lookup"><span data-stu-id="5f383-103">ITipAutocompleteClient interface</span></span>

<span data-ttu-id="5f383-104">可讓用戶端呼叫應用程式的文字輸入面板自動完成提供者物件。</span><span class="sxs-lookup"><span data-stu-id="5f383-104">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span>

## <a name="members"></a><span data-ttu-id="5f383-105">成員</span><span class="sxs-lookup"><span data-stu-id="5f383-105">Members</span></span>

<span data-ttu-id="5f383-106">**ITipAutocompleteClient** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5f383-106">The **ITipAutocompleteClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5f383-107">**ITipAutocompleteClient** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5f383-107">**ITipAutocompleteClient** also has these types of members:</span></span>

-   [<span data-ttu-id="5f383-108">方法</span><span class="sxs-lookup"><span data-stu-id="5f383-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5f383-109">方法</span><span class="sxs-lookup"><span data-stu-id="5f383-109">Methods</span></span>

<span data-ttu-id="5f383-110">**ITipAutocompleteClient** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5f383-110">The **ITipAutocompleteClient** interface has these methods.</span></span>



| <span data-ttu-id="5f383-111">方法</span><span class="sxs-lookup"><span data-stu-id="5f383-111">Method</span></span>                                                              | <span data-ttu-id="5f383-112">描述</span><span class="sxs-lookup"><span data-stu-id="5f383-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f383-113">**AdviseProvider**</span><span class="sxs-lookup"><span data-stu-id="5f383-113">**AdviseProvider**</span></span>](itipautocompleteclient-adviseprovider.md)     | <span data-ttu-id="5f383-114">向用戶端註冊提供者，以讓用戶端呼叫應用程式的自動完成提供者物件。</span><span class="sxs-lookup"><span data-stu-id="5f383-114">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="5f383-115">**PreferredRects**</span><span class="sxs-lookup"><span data-stu-id="5f383-115">**PreferredRects**</span></span>](itipautocompleteclient-preferredrects.md)     | <span data-ttu-id="5f383-116">允許用戶端建議在何處放置自動完成清單，以避免重迭輸入面板。</span><span class="sxs-lookup"><span data-stu-id="5f383-116">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span><br/>                                               |
| [<span data-ttu-id="5f383-117">**RequestShowUI**</span><span class="sxs-lookup"><span data-stu-id="5f383-117">**RequestShowUI**</span></span>](itipautocompleteclient-requestshowui.md)       | <span data-ttu-id="5f383-118">決定輸入面板是否已準備好顯示自動完成清單。</span><span class="sxs-lookup"><span data-stu-id="5f383-118">Determines whether Input Panel is ready to have the auto complete list shown.</span></span><br/>                                                                             |
| [<span data-ttu-id="5f383-119">**UnadviseProvider**</span><span class="sxs-lookup"><span data-stu-id="5f383-119">**UnadviseProvider**</span></span>](itipautocompleteclient-unadviseprovider.md) | <span data-ttu-id="5f383-120">取消註冊相關聯的提供者。</span><span class="sxs-lookup"><span data-stu-id="5f383-120">Unregisters the associated provider.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="5f383-121">**UserSelection**</span><span class="sxs-lookup"><span data-stu-id="5f383-121">**UserSelection**</span></span>](itipautocompleteclient-userselection.md)       | <span data-ttu-id="5f383-122">通知輸入面板，使用者已在自動完成清單中選取某個內容，並捨棄尚未插入的所有剩餘文字。</span><span class="sxs-lookup"><span data-stu-id="5f383-122">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5f383-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f383-123">Requirements</span></span>



| <span data-ttu-id="5f383-124">需求</span><span class="sxs-lookup"><span data-stu-id="5f383-124">Requirement</span></span> | <span data-ttu-id="5f383-125">值</span><span class="sxs-lookup"><span data-stu-id="5f383-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f383-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f383-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5f383-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f383-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5f383-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f383-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5f383-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="5f383-129">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="5f383-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5f383-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f383-131"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="5f383-131"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5f383-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5f383-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f383-133"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f383-133"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



 

