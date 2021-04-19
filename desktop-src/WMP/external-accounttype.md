---
title: External. accountType
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 AccountType 屬性會抓取目前使用者的帳戶類型。
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Windows Media Player 的外部 accountType
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984131"
---
# <a name="externalaccounttype"></a><span data-ttu-id="bb7d7-106">External. accountType</span><span class="sxs-lookup"><span data-stu-id="bb7d7-106">External.accountType</span></span>

> [!Note]  
> <span data-ttu-id="bb7d7-107">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bb7d7-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bb7d7-109">**AccountType** 屬性會抓取目前使用者的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-109">The **accountType** property retrieves the account type of the current user.</span></span>

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a><span data-ttu-id="bb7d7-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="bb7d7-110">Possible Values</span></span>

<span data-ttu-id="bb7d7-111">這個屬性是代表帳戶類型的唯讀 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-111">This property is a read-only **String** that represents the account type.</span></span> <span data-ttu-id="bb7d7-112">代表不同帳戶類型的字串是由線上商店所定義。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-112">Strings that represent various account types are defined by the online store.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7d7-113">備註</span><span class="sxs-lookup"><span data-stu-id="bb7d7-113">Remarks</span></span>

<span data-ttu-id="bb7d7-114">這個屬性會藉由呼叫 [IWMPContentPartner：： GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) 方法（由線上商店的外掛程式所執行）來抓取帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-114">This property retrieves the account type by calling the [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="bb7d7-115">如果目前的使用者已登入線上商店，或外掛程式已快取使用者的認證，則 **getContentPartnerInfo** 方法可以判斷使用者的帳戶類型，並將其傳回 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-115">If the current user is logged in to the online store or the plug-in has cached the user's credentials, the **getContentPartnerInfo** method can determine the user's account type and return it to Windows Media Player.</span></span> <span data-ttu-id="bb7d7-116">帳戶類型是 Windows Media Player 不會解讀的字串。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-116">The account type is a string that Windows Media Player does not interpret.</span></span> <span data-ttu-id="bb7d7-117">相反地，Windows Media Player 會將來自線上商店之外掛程式的字串傳遞至線上商店的 [探索] 頁面上的腳本。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-117">Rather, Windows Media Player passes the string from the online store's plug-in to the script on the online store's discovery page.</span></span>

<span data-ttu-id="bb7d7-118">如果目前的使用者未登入線上商店，且線上商店的外掛程式沒有使用者的快取認證，則此屬性會在該情況下抓取 **getContentPartnerInfo** 方法所傳回的任何字串。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-118">If the current user is not logged in to the online store and the online store's plug-in does not have cached credentials for the user, this property retrieves whatever string the **getContentPartnerInfo** method returns in that situation.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7d7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb7d7-119">Requirements</span></span>



| <span data-ttu-id="bb7d7-120">需求</span><span class="sxs-lookup"><span data-stu-id="bb7d7-120">Requirement</span></span> | <span data-ttu-id="bb7d7-121">值</span><span class="sxs-lookup"><span data-stu-id="bb7d7-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7d7-122">版本</span><span class="sxs-lookup"><span data-stu-id="bb7d7-122">Version</span></span><br/> | <span data-ttu-id="bb7d7-123">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="bb7d7-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="bb7d7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bb7d7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="bb7d7-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb7d7-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7d7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb7d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7d7-127">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="bb7d7-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="bb7d7-128">**UserLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="bb7d7-128">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





