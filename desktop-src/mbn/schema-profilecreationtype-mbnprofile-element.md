---
description: 包含設定檔建立者的相關資訊。
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: ProfileCreationType (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113453"
---
# <a name="profilecreationtype-mbnprofile-element"></a><span data-ttu-id="d1161-103">ProfileCreationType (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="d1161-103">ProfileCreationType (MBNProfile) Element</span></span>

<span data-ttu-id="d1161-104">**ProfileCreationType (MBNProfile)** 元素包含設定檔建立者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1161-104">The **ProfileCreationType (MBNProfile)** element contains information about the creator of the profile.</span></span>

<span data-ttu-id="d1161-105">這個元素可以具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d1161-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="d1161-106">值</span><span class="sxs-lookup"><span data-stu-id="d1161-106">Value</span></span>                 | <span data-ttu-id="d1161-107">意義</span><span class="sxs-lookup"><span data-stu-id="d1161-107">Meaning</span></span>                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1161-108">"UserProvisioned"</span><span class="sxs-lookup"><span data-stu-id="d1161-108">"UserProvisioned"</span></span>     | <span data-ttu-id="d1161-109">此設定檔是由裝置使用者提供的資訊所建立。</span><span class="sxs-lookup"><span data-stu-id="d1161-109">This profile is created by information provided by the user of device.</span></span>                                                     |
| <span data-ttu-id="d1161-110">"AdminProvisioned"</span><span class="sxs-lookup"><span data-stu-id="d1161-110">"AdminProvisioned"</span></span>    | <span data-ttu-id="d1161-111">此設定檔是由 IT 系統管理員所建立，並散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="d1161-111">This profile is created by IT administrators and distributed to users.</span></span>                                                     |
| <span data-ttu-id="d1161-112">"OperatorProvisioned"</span><span class="sxs-lookup"><span data-stu-id="d1161-112">"OperatorProvisioned"</span></span> | <span data-ttu-id="d1161-113">此設定檔是由網路操作員建立並散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="d1161-113">This profile is created by a network operator and distributed to users.</span></span>                                                    |
| <span data-ttu-id="d1161-114">"DeviceProvisioned"</span><span class="sxs-lookup"><span data-stu-id="d1161-114">"DeviceProvisioned"</span></span>   | <span data-ttu-id="d1161-115">此設定檔是由行動寬頻服務使用儲存在裝置布建內容中的資訊所建立。</span><span class="sxs-lookup"><span data-stu-id="d1161-115">This profile is created by the Mobile Broadband service by using the information stored in the device provisioned context.</span></span> |



 

<span data-ttu-id="d1161-116">這是選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="d1161-116">This is an optional element.</span></span>

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="d1161-117">**ProfileCreationType** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="d1161-117">The **ProfileCreationType** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1161-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1161-118">Requirements</span></span>



| <span data-ttu-id="d1161-119">需求</span><span class="sxs-lookup"><span data-stu-id="d1161-119">Requirement</span></span> | <span data-ttu-id="d1161-120">值</span><span class="sxs-lookup"><span data-stu-id="d1161-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d1161-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1161-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1161-122">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1161-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d1161-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1161-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1161-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="d1161-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d1161-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1161-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1161-126">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="d1161-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d1161-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d1161-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="d1161-128">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="d1161-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d1161-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d1161-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




