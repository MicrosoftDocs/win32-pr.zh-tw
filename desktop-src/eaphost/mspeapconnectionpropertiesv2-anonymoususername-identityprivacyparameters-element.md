---
title: AnonymousUserName (IdentityPrivacyParameters) 元素
description: 包含用來取代使用者真正識別的匿名身分識別。 當身分識別以純文字傳送時，會在 PEAP 驗證的第一個階段傳送。
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- AnonymousUserName 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384945"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a><span data-ttu-id="52493-105">AnonymousUserName (IdentityPrivacyParameters) 元素</span><span class="sxs-lookup"><span data-stu-id="52493-105">AnonymousUserName (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="52493-106">**AnonymousUserName (IdentityPrivacyParameters)** 元素包含用來取代使用者真正識別的匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="52493-106">The **AnonymousUserName (IdentityPrivacyParameters)** element contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="52493-107">當身分 **識別** 以純文字傳送時，會在 PEAP 驗證的第一個階段傳送。</span><span class="sxs-lookup"><span data-stu-id="52493-107">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span>

<span data-ttu-id="52493-108">匿名身分識別的使用方式取決於 [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="52493-108">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

<span data-ttu-id="52493-109">**AnonymousUserName** 元素是由 [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)定義。</span><span class="sxs-lookup"><span data-stu-id="52493-109">The **AnonymousUserName** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="52493-110">備註</span><span class="sxs-lookup"><span data-stu-id="52493-110">Remarks</span></span>

<span data-ttu-id="52493-111">**AnonymousUserName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="52493-111">The **AnonymousUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="52493-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="52493-112">Requirements</span></span>



| <span data-ttu-id="52493-113">需求</span><span class="sxs-lookup"><span data-stu-id="52493-113">Requirement</span></span> | <span data-ttu-id="52493-114">值</span><span class="sxs-lookup"><span data-stu-id="52493-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="52493-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52493-115">Minimum supported client</span></span><br/> | <span data-ttu-id="52493-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52493-116">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="52493-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52493-117">Minimum supported server</span></span><br/> | <span data-ttu-id="52493-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52493-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52493-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52493-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="52493-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="52493-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="52493-121">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="52493-121">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="52493-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="52493-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="52493-123">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="52493-123">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="52493-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="52493-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="52493-125">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="52493-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="52493-126">mspeapconnectionpropertiesv2 架構元素</span><span class="sxs-lookup"><span data-stu-id="52493-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





