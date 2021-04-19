---
title: UserLoggedIn
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |UserLoggedIn
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- UserLoggedIn Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976083"
---
# <a name="externaluserloggedin"></a><span data-ttu-id="14b22-105">UserLoggedIn</span><span class="sxs-lookup"><span data-stu-id="14b22-105">External.userLoggedIn</span></span>

> [!Note]  
> <span data-ttu-id="14b22-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="14b22-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="14b22-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="14b22-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="14b22-108">**UserLoggedIn** 屬性會抓取一個值，指出使用者是否已登入線上商店。</span><span class="sxs-lookup"><span data-stu-id="14b22-108">The **userLoggedIn** property retrieves a value indicating whether the user is logged in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b22-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="14b22-109">Syntax</span></span>

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a><span data-ttu-id="14b22-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="14b22-110">Possible Values</span></span>

<span data-ttu-id="14b22-111">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="14b22-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="14b22-112">**TRUE** 表示使用者已登入，而 **FALSE** 表示使用者已登出。</span><span class="sxs-lookup"><span data-stu-id="14b22-112">**TRUE** indicates that the user is logged in, and **FALSE** indicates that the user is logged out.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b22-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="14b22-113">Requirements</span></span>



| <span data-ttu-id="14b22-114">需求</span><span class="sxs-lookup"><span data-stu-id="14b22-114">Requirement</span></span> | <span data-ttu-id="14b22-115">值</span><span class="sxs-lookup"><span data-stu-id="14b22-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14b22-116">版本</span><span class="sxs-lookup"><span data-stu-id="14b22-116">Version</span></span><br/> | <span data-ttu-id="14b22-117">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="14b22-117">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="14b22-118">DLL</span><span class="sxs-lookup"><span data-stu-id="14b22-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="14b22-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b22-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b22-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14b22-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b22-121">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="14b22-121">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="14b22-122">**AttemptLogin**</span><span class="sxs-lookup"><span data-stu-id="14b22-122">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="14b22-123">**OnLoginChange 事件**</span><span class="sxs-lookup"><span data-stu-id="14b22-123">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> </dl>

 

 





