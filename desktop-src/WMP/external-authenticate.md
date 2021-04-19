---
title: External. 驗證方法
description: 驗證方法會起始驗證使用者的嘗試。
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- 驗證方法 Windows Media Player
- 驗證方法 Windows Media Player、外部類別
- 外部類別 Windows Media Player，驗證方法
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977531"
---
# <a name="externalauthenticate-method"></a><span data-ttu-id="10e07-106">External. 驗證方法</span><span class="sxs-lookup"><span data-stu-id="10e07-106">External.authenticate method</span></span>

<span data-ttu-id="10e07-107">**驗證** 方法會起始驗證使用者的嘗試。</span><span class="sxs-lookup"><span data-stu-id="10e07-107">The **authenticate** method initiates an attempt to authenticate the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e07-108">語法</span><span class="sxs-lookup"><span data-stu-id="10e07-108">Syntax</span></span>


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a><span data-ttu-id="10e07-109">參數</span><span class="sxs-lookup"><span data-stu-id="10e07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e07-110">*AuthenticationIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10e07-110">*AuthenticationIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e07-111">指定驗證-成功網頁索引的 (**long**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="10e07-111">**Number** (**long**) that specifies the index of an authentication-success webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e07-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="10e07-112">Return value</span></span>

<span data-ttu-id="10e07-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10e07-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10e07-114">備註</span><span class="sxs-lookup"><span data-stu-id="10e07-114">Remarks</span></span>

<span data-ttu-id="10e07-115">[探索] 頁面上的某些連結具有應只在使用者經過驗證之後才顯示的目標。</span><span class="sxs-lookup"><span data-stu-id="10e07-115">Certain links on a discovery page have targets that should be displayed only after the user has been authenticated.</span></span> <span data-ttu-id="10e07-116">[探索] 頁面、Windows Media Player 和線上商店的外掛程式會使用下列步驟來驗證使用者，並顯示目標網頁：</span><span class="sxs-lookup"><span data-stu-id="10e07-116">The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:</span></span>

1.  <span data-ttu-id="10e07-117">探索頁面上的腳本會呼叫 *External*。**驗證** 方法。</span><span class="sxs-lookup"><span data-stu-id="10e07-117">Script on a discovery page calls the *External*.**authenticate** method.</span></span>
2.  <span data-ttu-id="10e07-118">Windows Media Player 會顯示一個對話方塊，以取得使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="10e07-118">Windows Media Player displays a dialog box to obtain a user name and password.</span></span>
3.  <span data-ttu-id="10e07-119">Windows Media Player 會呼叫 [IWMPContentPartner：：](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate)authentication，此動作會起始驗證嘗試，並立即傳回。</span><span class="sxs-lookup"><span data-stu-id="10e07-119">Windows Media Player calls [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), which initiates the authentication attempt and returns immediately.</span></span>
4.  <span data-ttu-id="10e07-120">當驗證嘗試完成時，線上商店的外掛程式會呼叫 [IWMPContentPartnerCallback：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)，傳遞 wmpcnAuthResult 和指出嘗試是否成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="10e07-120">When the authentication attempt is complete, the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</span></span>
5.  <span data-ttu-id="10e07-121">如果驗證嘗試成功，Windows Media Player 會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，傳遞 g \_ szItemInfo \_ AuthenticationSuccessURL，以取得驗證成功網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="10e07-121">If the authentication attempt was successful, Windows Media Player calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage.</span></span> <span data-ttu-id="10e07-122">在此呼叫中，Windows Media Player 會傳遞探索頁面傳遞給 *外部* 的相同索引。**驗證** 方法。</span><span class="sxs-lookup"><span data-stu-id="10e07-122">In this call, Windows Media Player passes the same index that the discovery page passed to the *External*.**authenticate** method.</span></span>
6.  <span data-ttu-id="10e07-123">Windows Media Player 顯示驗證-成功網頁。</span><span class="sxs-lookup"><span data-stu-id="10e07-123">Windows Media Player displays the authentication-success webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e07-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="10e07-124">Requirements</span></span>



| <span data-ttu-id="10e07-125">需求</span><span class="sxs-lookup"><span data-stu-id="10e07-125">Requirement</span></span> | <span data-ttu-id="10e07-126">值</span><span class="sxs-lookup"><span data-stu-id="10e07-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10e07-127">版本</span><span class="sxs-lookup"><span data-stu-id="10e07-127">Version</span></span><br/> | <span data-ttu-id="10e07-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="10e07-128">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="10e07-129">DLL</span><span class="sxs-lookup"><span data-stu-id="10e07-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="10e07-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10e07-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10e07-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10e07-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e07-132">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="10e07-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="10e07-133">**AttemptLogin**</span><span class="sxs-lookup"><span data-stu-id="10e07-133">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="10e07-134">**UserLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="10e07-134">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





