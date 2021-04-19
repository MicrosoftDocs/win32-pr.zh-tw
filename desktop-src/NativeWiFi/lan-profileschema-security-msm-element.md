---
description: 包含有線網路的安全性設定。
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: '安全性 (.MSM) 元素 (LAN_policy) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106986553"
---
# <a name="security-msm-element-lan_policy"></a><span data-ttu-id="3a7ab-103">安全性 (.MSM) 元素 (LAN_policy) </span><span class="sxs-lookup"><span data-stu-id="3a7ab-103">Security (MSM) Element (LAN_policy)</span></span>

<span data-ttu-id="3a7ab-104">安全性 (.MSM) 元素包含有線網路的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="3a7ab-104">The security (MSM) element contains security settings for wired networks.</span></span> <span data-ttu-id="3a7ab-105">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="3a7ab-105">This element is optional.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="3a7ab-106">**安全性** 元素是由 [**MSM**](lan-profileschema-msm-lanprofile-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="3a7ab-106">The **security** element is defined by the [**MSM**](lan-profileschema-msm-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3a7ab-107">子元素</span><span class="sxs-lookup"><span data-stu-id="3a7ab-107">Child elements</span></span>



| <span data-ttu-id="3a7ab-108">元素</span><span class="sxs-lookup"><span data-stu-id="3a7ab-108">Element</span></span>                                                                 | <span data-ttu-id="3a7ab-109">類型</span><span class="sxs-lookup"><span data-stu-id="3a7ab-109">Type</span></span>    | <span data-ttu-id="3a7ab-110">Description</span><span class="sxs-lookup"><span data-stu-id="3a7ab-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a7ab-111">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="3a7ab-111">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="3a7ab-112">boolean</span><span class="sxs-lookup"><span data-stu-id="3a7ab-112">boolean</span></span> | <span data-ttu-id="3a7ab-113">指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="3a7ab-113">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="3a7ab-114">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="3a7ab-114">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="3a7ab-115">boolean</span><span class="sxs-lookup"><span data-stu-id="3a7ab-115">boolean</span></span> | <span data-ttu-id="3a7ab-116">指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="3a7ab-116">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="3a7ab-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a7ab-117">Requirements</span></span>



| <span data-ttu-id="3a7ab-118">需求</span><span class="sxs-lookup"><span data-stu-id="3a7ab-118">Requirement</span></span> | <span data-ttu-id="3a7ab-119">值</span><span class="sxs-lookup"><span data-stu-id="3a7ab-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a7ab-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a7ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a7ab-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a7ab-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a7ab-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a7ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a7ab-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a7ab-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a7ab-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a7ab-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a7ab-125">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="3a7ab-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3a7ab-126">**MSM**</span><span class="sxs-lookup"><span data-stu-id="3a7ab-126">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="3a7ab-127">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="3a7ab-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3a7ab-128">**MSM (LANProfile)**</span><span class="sxs-lookup"><span data-stu-id="3a7ab-128">**MSM (LANProfile)**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




