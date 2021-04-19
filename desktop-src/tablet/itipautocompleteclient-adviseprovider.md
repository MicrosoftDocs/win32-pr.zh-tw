---
description: 向用戶端註冊提供者，以讓用戶端呼叫應用程式的自動完成提供者物件。
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'ITipAutocompleteClient：： AdviseProvider 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981619"
---
# <a name="itipautocompleteclientadviseprovider-method"></a><span data-ttu-id="cc8e9-103">ITipAutocompleteClient：： AdviseProvider 方法</span><span class="sxs-lookup"><span data-stu-id="cc8e9-103">ITipAutocompleteClient::AdviseProvider method</span></span>

<span data-ttu-id="cc8e9-104">向用戶端註冊提供者，以讓用戶端呼叫應用程式的自動完成提供者物件。</span><span class="sxs-lookup"><span data-stu-id="cc8e9-104">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc8e9-105">Syntax</span></span>


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="cc8e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc8e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc8e9-107">*hWndField* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc8e9-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc8e9-108">提供自動完成功能的欄位的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="cc8e9-108">The window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="cc8e9-109">*pIACProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc8e9-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc8e9-110">自動完成提供者介面的介面指標。</span><span class="sxs-lookup"><span data-stu-id="cc8e9-110">The interface pointer to the auto complete provider interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc8e9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc8e9-111">Return value</span></span>

<span data-ttu-id="cc8e9-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cc8e9-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cc8e9-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cc8e9-113">Return code</span></span>                                                                            | <span data-ttu-id="cc8e9-114">Description</span><span class="sxs-lookup"><span data-stu-id="cc8e9-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="cc8e9-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="cc8e9-116">成功。</span><span class="sxs-lookup"><span data-stu-id="cc8e9-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="cc8e9-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="cc8e9-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cc8e9-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cc8e9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc8e9-119">Requirements</span></span>



| <span data-ttu-id="cc8e9-120">需求</span><span class="sxs-lookup"><span data-stu-id="cc8e9-120">Requirement</span></span> | <span data-ttu-id="cc8e9-121">值</span><span class="sxs-lookup"><span data-stu-id="cc8e9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8e9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc8e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8e9-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc8e9-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="cc8e9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc8e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8e9-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="cc8e9-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="cc8e9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="cc8e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc8e9-127"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cc8e9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cc8e9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc8e9-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="cc8e9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc8e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8e9-131">**ITipAutocompleteClient 介面**</span><span class="sxs-lookup"><span data-stu-id="cc8e9-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="cc8e9-132">**ITipAutocompleteClient：： UnadviseProvider 方法**</span><span class="sxs-lookup"><span data-stu-id="cc8e9-132">**ITipAutocompleteClient::UnadviseProvider Method**</span></span>](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[<span data-ttu-id="cc8e9-133">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="cc8e9-133">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




