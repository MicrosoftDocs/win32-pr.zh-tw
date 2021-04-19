---
description: 指定無線區域網路上所使用的802.11 無線區域網路標準。
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: phyType (連接) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992405"
---
# <a name="phytype-connectivity-element"></a><span data-ttu-id="6836c-103">phyType (連接) 元素</span><span class="sxs-lookup"><span data-stu-id="6836c-103">phyType (connectivity) Element</span></span>

<span data-ttu-id="6836c-104">PhyType (connectivity) 元素會指定無線區域網路上所使用的802.11 無線區域網路標準。</span><span class="sxs-lookup"><span data-stu-id="6836c-104">The phyType (connectivity) element specifies the 802.11 wireless LAN standard used on a wireless LAN.</span></span>

<span data-ttu-id="6836c-105">您可以指定多個 **phyType**。</span><span class="sxs-lookup"><span data-stu-id="6836c-105">You can specify multiple **phyType** s.</span></span> <span data-ttu-id="6836c-106">如果未指定任何 **phyType** ，則可以使用設定檔來連接至任何 **phyType**。</span><span class="sxs-lookup"><span data-stu-id="6836c-106">If no **phyType** is specified, the profile can be used to connect to any **phyType**.</span></span> <span data-ttu-id="6836c-107">只有在 Windows Vista Service Pack 1 (SP1) 和更新版本的作業系統上，才支援值 "n"。</span><span class="sxs-lookup"><span data-stu-id="6836c-107">The value "n" is only supported on Windows Vista with Service Pack 1 (SP1) and later versions of the operating system.</span></span>

<span data-ttu-id="6836c-108">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="6836c-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="6836c-109">專案是由 [**connectivity**](wlan-profileschema-connectivity-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="6836c-109">The element is defined by the [**connectivity**](wlan-profileschema-connectivity-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6836c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6836c-110">Requirements</span></span>



| <span data-ttu-id="6836c-111">需求</span><span class="sxs-lookup"><span data-stu-id="6836c-111">Requirement</span></span> | <span data-ttu-id="6836c-112">值</span><span class="sxs-lookup"><span data-stu-id="6836c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6836c-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6836c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6836c-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6836c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6836c-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6836c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6836c-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6836c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6836c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6836c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6836c-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="6836c-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6836c-119">**連接**</span><span class="sxs-lookup"><span data-stu-id="6836c-119">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

<span data-ttu-id="6836c-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="6836c-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6836c-121">**(MSM) 的連線能力**</span><span class="sxs-lookup"><span data-stu-id="6836c-121">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




