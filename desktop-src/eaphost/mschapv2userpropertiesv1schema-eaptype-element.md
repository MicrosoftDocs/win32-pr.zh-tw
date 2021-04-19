---
title: 'EapType 元素 (mschapv2userpropertiesv1schema) '
description: 這個元素是 baseeapuserpropertiesv1 架構中 EapType 元素的衍生型別。 適用于 mschapv2userpropertiesv1schema。
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
keywords:
- EapType 元素 EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106981414"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a><span data-ttu-id="2ee77-105">EapType 元素 (mschapv2userpropertiesv1schema) </span><span class="sxs-lookup"><span data-stu-id="2ee77-105">EapType element (mschapv2userpropertiesv1schema)</span></span>

<span data-ttu-id="2ee77-106">**EapType** 元素是 [Baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md)元素的衍生型別。</span><span class="sxs-lookup"><span data-stu-id="2ee77-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="2ee77-107">子元素</span><span class="sxs-lookup"><span data-stu-id="2ee77-107">Child elements</span></span>



| <span data-ttu-id="2ee77-108">元素</span><span class="sxs-lookup"><span data-stu-id="2ee77-108">Element</span></span>                                                                           | <span data-ttu-id="2ee77-109">類型</span><span class="sxs-lookup"><span data-stu-id="2ee77-109">Type</span></span>   | <span data-ttu-id="2ee77-110">Description</span><span class="sxs-lookup"><span data-stu-id="2ee77-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ee77-111">**使用者**</span><span class="sxs-lookup"><span data-stu-id="2ee77-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="2ee77-112">識別要驗證的使用者。</span><span class="sxs-lookup"><span data-stu-id="2ee77-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="2ee77-113">如果這個元素不存在，則會從 winlogon 取得使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee77-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="2ee77-114">[**Username**](mschapv2userpropertiesv1schema-username-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ee77-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="2ee77-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="2ee77-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="2ee77-116">字串</span><span class="sxs-lookup"><span data-stu-id="2ee77-116">string</span></span> | <span data-ttu-id="2ee77-117">識別要驗證之使用者或電腦的網域。</span><span class="sxs-lookup"><span data-stu-id="2ee77-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="2ee77-118">如果此元素不存在，則會使用 winlogon 的網域。</span><span class="sxs-lookup"><span data-stu-id="2ee77-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="2ee77-119">[**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ee77-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="2ee77-120">**密碼**</span><span class="sxs-lookup"><span data-stu-id="2ee77-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="2ee77-121">字串</span><span class="sxs-lookup"><span data-stu-id="2ee77-121">string</span></span> | <span data-ttu-id="2ee77-122">識別要驗證之使用者或電腦的密碼。</span><span class="sxs-lookup"><span data-stu-id="2ee77-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="2ee77-123">如果這個元素不存在，則會從 winlogon 取得密碼雜湊。</span><span class="sxs-lookup"><span data-stu-id="2ee77-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="2ee77-124">[**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ee77-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2ee77-125">備註</span><span class="sxs-lookup"><span data-stu-id="2ee77-125">Remarks</span></span>

<span data-ttu-id="2ee77-126">**ProcessContents** 元素可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="2ee77-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="2ee77-127">**ProcessContents** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2ee77-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee77-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ee77-128">Requirements</span></span>



| <span data-ttu-id="2ee77-129">需求</span><span class="sxs-lookup"><span data-stu-id="2ee77-129">Requirement</span></span> | <span data-ttu-id="2ee77-130">值</span><span class="sxs-lookup"><span data-stu-id="2ee77-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ee77-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ee77-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee77-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ee77-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2ee77-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ee77-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee77-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ee77-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ee77-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ee77-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee77-136">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="2ee77-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2ee77-137">mschapv2userpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="2ee77-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





