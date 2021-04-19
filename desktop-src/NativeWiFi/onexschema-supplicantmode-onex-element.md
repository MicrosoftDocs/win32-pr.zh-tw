---
description: 指定用於 EAPOL-Start 訊息的傳輸方法。
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: supplicantMode (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989390"
---
# <a name="supplicantmode-onex-element"></a><span data-ttu-id="beee6-103">supplicantMode (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="beee6-103">supplicantMode (OneX) Element</span></span>

<span data-ttu-id="beee6-104">SupplicantMode (OneX) 元素會指定用於 EAPOL-Start 訊息的傳輸方法。</span><span class="sxs-lookup"><span data-stu-id="beee6-104">The supplicantMode (OneX) element specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="beee6-105">下表說明可能出現的值。</span><span class="sxs-lookup"><span data-stu-id="beee6-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="beee6-106">值</span><span class="sxs-lookup"><span data-stu-id="beee6-106">Value</span></span>               | <span data-ttu-id="beee6-107">描述</span><span class="sxs-lookup"><span data-stu-id="beee6-107">Description</span></span>                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beee6-108">inhibitTransmission</span><span class="sxs-lookup"><span data-stu-id="beee6-108">inhibitTransmission</span></span> | <span data-ttu-id="beee6-109">EAPOL-Start 不會傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="beee6-109">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="beee6-110">僅適用于有線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="beee6-110">Valid for wired LAN profiles only.</span></span>                                                                                             |
| <span data-ttu-id="beee6-111">includeLearning</span><span class="sxs-lookup"><span data-stu-id="beee6-111">includeLearning</span></span>     | <span data-ttu-id="beee6-112">用戶端會根據網路功能決定傳送 EAPOL-Start 封包的時機。</span><span class="sxs-lookup"><span data-stu-id="beee6-112">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="beee6-113">EAPOL-Start 訊息只會在必要時傳送。</span><span class="sxs-lookup"><span data-stu-id="beee6-113">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="beee6-114">僅適用于有線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="beee6-114">Valid for wired LAN profiles only.</span></span> |
| <span data-ttu-id="beee6-115">compliant</span><span class="sxs-lookup"><span data-stu-id="beee6-115">compliant</span></span>           | <span data-ttu-id="beee6-116">EAPOL-Start 的訊息會由 802.1 X 所指定的方式傳輸。</span><span class="sxs-lookup"><span data-stu-id="beee6-116">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="beee6-117">適用于有線和無線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="beee6-117">Valid for both wired and wireless LAN profiles.</span></span>                                                             |



 

<span data-ttu-id="beee6-118">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="beee6-118">This element is optional.</span></span> <span data-ttu-id="beee6-119">當設定檔中未指定 supplicantMode 時，會將的值 `compliant` 用於有線和無線局域網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="beee6-119">When supplicantMode is not specified in a profile, a value of `compliant` is used for both wired and wireless LAN profiles.</span></span>

<span data-ttu-id="beee6-120">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="beee6-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="beee6-121">**SupplicantMode** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="beee6-121">The **supplicantMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="beee6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="beee6-122">Requirements</span></span>



| <span data-ttu-id="beee6-123">需求</span><span class="sxs-lookup"><span data-stu-id="beee6-123">Requirement</span></span> | <span data-ttu-id="beee6-124">值</span><span class="sxs-lookup"><span data-stu-id="beee6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="beee6-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="beee6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="beee6-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="beee6-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="beee6-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="beee6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="beee6-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="beee6-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="beee6-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="beee6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="beee6-130">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="beee6-130">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="beee6-131">**OneX**</span><span class="sxs-lookup"><span data-stu-id="beee6-131">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="beee6-132">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="beee6-132">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="beee6-133">**OneX**</span><span class="sxs-lookup"><span data-stu-id="beee6-133">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




