---
description: 通知輸入面板，使用者已在自動完成清單中選取某個內容，並捨棄尚未插入的所有剩餘文字。
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'ITipAutocompleteClient：： UserSelection 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977062"
---
# <a name="itipautocompleteclientuserselection-method"></a><span data-ttu-id="7dc15-103">ITipAutocompleteClient：： UserSelection 方法</span><span class="sxs-lookup"><span data-stu-id="7dc15-103">ITipAutocompleteClient::UserSelection method</span></span>

<span data-ttu-id="7dc15-104">通知輸入面板，使用者已在自動完成清單中選取某個內容，並捨棄尚未插入的所有剩餘文字。</span><span class="sxs-lookup"><span data-stu-id="7dc15-104">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc15-105">語法</span><span class="sxs-lookup"><span data-stu-id="7dc15-105">Syntax</span></span>


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a><span data-ttu-id="7dc15-106">參數</span><span class="sxs-lookup"><span data-stu-id="7dc15-106">Parameters</span></span>

<span data-ttu-id="7dc15-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7dc15-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7dc15-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dc15-108">Return value</span></span>

<span data-ttu-id="7dc15-109">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7dc15-109">This method can return one of these values.</span></span>



| <span data-ttu-id="7dc15-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7dc15-110">Return code</span></span>                                                                            | <span data-ttu-id="7dc15-111">Description</span><span class="sxs-lookup"><span data-stu-id="7dc15-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7dc15-112"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7dc15-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7dc15-113">成功。</span><span class="sxs-lookup"><span data-stu-id="7dc15-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7dc15-114"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="7dc15-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7dc15-115">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7dc15-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7dc15-116">備註</span><span class="sxs-lookup"><span data-stu-id="7dc15-116">Remarks</span></span>

<span data-ttu-id="7dc15-117">從提供者呼叫這個方法，以通知用戶端已由使用者進行選取。</span><span class="sxs-lookup"><span data-stu-id="7dc15-117">This method is called from the provider to notify the client that a selection has been made by the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc15-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dc15-118">Requirements</span></span>



| <span data-ttu-id="7dc15-119">需求</span><span class="sxs-lookup"><span data-stu-id="7dc15-119">Requirement</span></span> | <span data-ttu-id="7dc15-120">值</span><span class="sxs-lookup"><span data-stu-id="7dc15-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc15-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dc15-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc15-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dc15-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7dc15-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dc15-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc15-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="7dc15-124">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="7dc15-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7dc15-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc15-126"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7dc15-126"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7dc15-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7dc15-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dc15-128"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dc15-128"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="7dc15-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dc15-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc15-130">**ITipAutocompleteClient 介面**</span><span class="sxs-lookup"><span data-stu-id="7dc15-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="7dc15-131">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="7dc15-131">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




