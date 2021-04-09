---
description: 取消註冊相關聯的提供者。
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'ITipAutocompleteClient：： UnadviseProvider 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849704"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a><span data-ttu-id="3d35d-103">ITipAutocompleteClient：： UnadviseProvider 方法</span><span class="sxs-lookup"><span data-stu-id="3d35d-103">ITipAutocompleteClient::UnadviseProvider method</span></span>

<span data-ttu-id="3d35d-104">取消註冊相關聯的提供者。</span><span class="sxs-lookup"><span data-stu-id="3d35d-104">Unregisters the associated provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d35d-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d35d-105">Syntax</span></span>


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="3d35d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d35d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d35d-107">*hWndField* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d35d-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d35d-108">提供自動完成功能之欄位的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="3d35d-108">Window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="3d35d-109">*pIACProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d35d-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d35d-110">要取消註冊之自動完成提供者介面的介面指標。</span><span class="sxs-lookup"><span data-stu-id="3d35d-110">Interface pointer to the auto complete provider interface to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d35d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d35d-111">Return value</span></span>

<span data-ttu-id="3d35d-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3d35d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3d35d-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3d35d-113">Return code</span></span>                                                                            | <span data-ttu-id="3d35d-114">Description</span><span class="sxs-lookup"><span data-stu-id="3d35d-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3d35d-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3d35d-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3d35d-116">成功。</span><span class="sxs-lookup"><span data-stu-id="3d35d-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3d35d-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="3d35d-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3d35d-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3d35d-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3d35d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d35d-119">Requirements</span></span>



| <span data-ttu-id="3d35d-120">需求</span><span class="sxs-lookup"><span data-stu-id="3d35d-120">Requirement</span></span> | <span data-ttu-id="3d35d-121">值</span><span class="sxs-lookup"><span data-stu-id="3d35d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d35d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d35d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d35d-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d35d-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="3d35d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d35d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d35d-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="3d35d-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="3d35d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3d35d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d35d-127"><dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3d35d-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3d35d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3d35d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d35d-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d35d-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="3d35d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d35d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d35d-131">**ITipAutocompleteClient 介面**</span><span class="sxs-lookup"><span data-stu-id="3d35d-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="3d35d-132">文字輸入面板參考</span><span class="sxs-lookup"><span data-stu-id="3d35d-132">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




