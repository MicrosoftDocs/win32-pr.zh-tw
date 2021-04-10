---
title: '隱私權類型 (Wininet. h) '
description: 指定隱私權設定適用于第一方或協力廠商 cookie。
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844375"
---
# <a name="privacy-type"></a><span data-ttu-id="cb053-103">隱私權類型</span><span class="sxs-lookup"><span data-stu-id="cb053-103">Privacy Type</span></span>

<span data-ttu-id="cb053-104">指定隱私權設定適用于第一方或協力廠商 cookie。</span><span class="sxs-lookup"><span data-stu-id="cb053-104">Specifies that privacy settings are for either first-party or third-party cookies.</span></span>

<dl> <dt>

<span data-ttu-id="cb053-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**隱私權 \_ 類型 \_ 第一 \_ 方**</span><span class="sxs-lookup"><span data-stu-id="cb053-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY\_TYPE\_FIRST\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb053-106">0</span><span class="sxs-lookup"><span data-stu-id="cb053-106">0</span></span>
</dt> <dt>



<span data-ttu-id="cb053-107">是指第一方 cookie 的隱私權設定。</span><span class="sxs-lookup"><span data-stu-id="cb053-107">Refers to privacy settings for first party cookies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cb053-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**隱私權 \_ 類型 \_ 第三 \_ 方**</span><span class="sxs-lookup"><span data-stu-id="cb053-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY\_TYPE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb053-109">1</span><span class="sxs-lookup"><span data-stu-id="cb053-109">1</span></span>
</dt> <dt>



<span data-ttu-id="cb053-110">指的是協力廠商 cookie 的隱私權設定。</span><span class="sxs-lookup"><span data-stu-id="cb053-110">Refers to privacy settings for third party cookies.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb053-111">備註</span><span class="sxs-lookup"><span data-stu-id="cb053-111">Remarks</span></span>

<span data-ttu-id="cb053-112">Cookie 會分類為第一方和協力廠商。</span><span class="sxs-lookup"><span data-stu-id="cb053-112">Cookies are categorized as first-party and third-party.</span></span> <span data-ttu-id="cb053-113">第一方 cookie 是源自主機網域的 cookie。</span><span class="sxs-lookup"><span data-stu-id="cb053-113">A first-party cookie is one that originates from the host domain.</span></span> <span data-ttu-id="cb053-114">如果 https://www.blueyonderairlines.com 在 Microsoft Internet Explorer 網址列中找到 ""，則 "www.blueyonderairlines.com" 是主機網域。</span><span class="sxs-lookup"><span data-stu-id="cb053-114">If "https://www.blueyonderairlines.com" is found in the Microsoft Internet Explorer address bar, "www.blueyonderairlines.com" is the host domain.</span></span> <span data-ttu-id="cb053-115">造訪此頁面時，如果從 "www.blueyonderairlines.com" 以外的網域設定 cookie （例如 "www.fourthcoffee.com"），則會將此 cookie 視為協力廠商 cookie。</span><span class="sxs-lookup"><span data-stu-id="cb053-115">While visiting this page, if a cookie is set from a domain other than "www.blueyonderairlines.com", such as "www.fourthcoffee.com", this cookie is considered a third-party cookie.</span></span>

> [!Note]  
> <span data-ttu-id="cb053-116">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="cb053-116">WinINet does not support server implementations.</span></span> <span data-ttu-id="cb053-117">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="cb053-117">In addition, it should not be used from a service.</span></span> <span data-ttu-id="cb053-118">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="cb053-118">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb053-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb053-119">Requirements</span></span>



| <span data-ttu-id="cb053-120">需求</span><span class="sxs-lookup"><span data-stu-id="cb053-120">Requirement</span></span> | <span data-ttu-id="cb053-121">值</span><span class="sxs-lookup"><span data-stu-id="cb053-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb053-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb053-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb053-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb053-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cb053-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb053-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb053-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb053-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb053-126">標頭</span><span class="sxs-lookup"><span data-stu-id="cb053-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb053-127"><dt>Wininet</dt></span><span class="sxs-lookup"><span data-stu-id="cb053-127"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb053-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb053-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb053-129">**PrivacyGetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="cb053-129">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="cb053-130">**PrivacySetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="cb053-130">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

