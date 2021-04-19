---
title: AttemptLogin 方法
description: AttemptLogin 方法會顯示對話方塊，讓使用者可以嘗試登入線上商店。
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- attemptLogin 方法 Windows Media Player
- attemptLogin 方法 Windows Media Player、External 類別
- External class Windows Media Player，attemptLogin 方法
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976084"
---
# <a name="externalattemptlogin-method"></a><span data-ttu-id="93ec0-106">AttemptLogin 方法</span><span class="sxs-lookup"><span data-stu-id="93ec0-106">External.attemptLogin method</span></span>

<span data-ttu-id="93ec0-107">**AttemptLogin** 方法會顯示對話方塊，讓使用者可以嘗試登入線上商店。</span><span class="sxs-lookup"><span data-stu-id="93ec0-107">The **attemptLogin** method displays a dialog box so the user can attempt to log in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ec0-108">語法</span><span class="sxs-lookup"><span data-stu-id="93ec0-108">Syntax</span></span>


```JScript
External.attemptLogin()
```



## <a name="parameters"></a><span data-ttu-id="93ec0-109">參數</span><span class="sxs-lookup"><span data-stu-id="93ec0-109">Parameters</span></span>

<span data-ttu-id="93ec0-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="93ec0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93ec0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="93ec0-111">Return value</span></span>

<span data-ttu-id="93ec0-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="93ec0-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93ec0-113">備註</span><span class="sxs-lookup"><span data-stu-id="93ec0-113">Remarks</span></span>

<span data-ttu-id="93ec0-114">如果登入嘗試導致登入狀態的變更，Windows Media Player 會引發 [OnLoginChange](external-onloginchange-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="93ec0-114">If the log-in attempt results in a change of log-in status, Windows Media Player raises the [OnLoginChange](external-onloginchange-event.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ec0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="93ec0-115">Requirements</span></span>



| <span data-ttu-id="93ec0-116">需求</span><span class="sxs-lookup"><span data-stu-id="93ec0-116">Requirement</span></span> | <span data-ttu-id="93ec0-117">值</span><span class="sxs-lookup"><span data-stu-id="93ec0-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93ec0-118">版本</span><span class="sxs-lookup"><span data-stu-id="93ec0-118">Version</span></span><br/> | <span data-ttu-id="93ec0-119">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="93ec0-119">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="93ec0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="93ec0-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="93ec0-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93ec0-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ec0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ec0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ec0-123">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="93ec0-123">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="93ec0-124">**OnLoginChange 事件**</span><span class="sxs-lookup"><span data-stu-id="93ec0-124">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="93ec0-125">**UserLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="93ec0-125">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="93ec0-126">**IWMPContentPartner：： Login**</span><span class="sxs-lookup"><span data-stu-id="93ec0-126">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="93ec0-127">**管理登入**</span><span class="sxs-lookup"><span data-stu-id="93ec0-127">**Managing Login**</span></span>](managing-login.md)
</dt> </dl>

 

 





