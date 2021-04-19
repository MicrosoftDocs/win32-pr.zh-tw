---
description: 包含用來識別 IHV 的3個位元組 hexBinary。
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: OUI (OUIHeader) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973246"
---
# <a name="oui-ouiheader-element"></a><span data-ttu-id="74a0b-103">OUI (OUIHeader) 元素</span><span class="sxs-lookup"><span data-stu-id="74a0b-103">OUI (OUIHeader) Element</span></span>

<span data-ttu-id="74a0b-104">OUI (OUIHeader) 元素包含用來識別 IHV 的3個位元組 hexBinary。</span><span class="sxs-lookup"><span data-stu-id="74a0b-104">The OUI (OUIHeader) element contains a 3 byte hexBinary that identifies the IHV.</span></span>

<span data-ttu-id="74a0b-105">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="74a0b-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUI">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="74a0b-106">元素是由 [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="74a0b-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="74a0b-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="74a0b-107">Requirements</span></span>



| <span data-ttu-id="74a0b-108">需求</span><span class="sxs-lookup"><span data-stu-id="74a0b-108">Requirement</span></span> | <span data-ttu-id="74a0b-109">值</span><span class="sxs-lookup"><span data-stu-id="74a0b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74a0b-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74a0b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="74a0b-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74a0b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74a0b-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74a0b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="74a0b-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74a0b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74a0b-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74a0b-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="74a0b-115">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="74a0b-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="74a0b-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="74a0b-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="74a0b-117">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="74a0b-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="74a0b-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="74a0b-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




