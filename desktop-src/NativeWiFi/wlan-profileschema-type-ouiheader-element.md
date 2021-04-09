---
description: 包含1位元組的 hexBinary，用來區別相同 IHV 所建立的 Nic。
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: 輸入 (OUIHeader) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849912"
---
# <a name="type-ouiheader-element"></a><span data-ttu-id="957bb-103">輸入 (OUIHeader) 元素</span><span class="sxs-lookup"><span data-stu-id="957bb-103">type (OUIHeader) Element</span></span>

<span data-ttu-id="957bb-104">類型 (OUIHeader) 元素包含1個位元組的 hexBinary，可用來區別相同 IHV 所建立的 Nic。</span><span class="sxs-lookup"><span data-stu-id="957bb-104">The type (OUIHeader) element contains a 1-byte hexBinary that is used to differentiate between NICs made by the same IHV.</span></span>

<span data-ttu-id="957bb-105">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="957bb-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="type">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="957bb-106">元素是由 [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="957bb-106">The element is defined by the [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="957bb-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="957bb-107">Requirements</span></span>



| <span data-ttu-id="957bb-108">需求</span><span class="sxs-lookup"><span data-stu-id="957bb-108">Requirement</span></span> | <span data-ttu-id="957bb-109">值</span><span class="sxs-lookup"><span data-stu-id="957bb-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="957bb-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="957bb-110">Minimum supported client</span></span><br/> | <span data-ttu-id="957bb-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="957bb-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="957bb-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="957bb-112">Minimum supported server</span></span><br/> | <span data-ttu-id="957bb-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="957bb-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="957bb-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="957bb-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="957bb-115">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="957bb-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="957bb-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="957bb-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

<span data-ttu-id="957bb-117">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="957bb-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="957bb-118">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="957bb-118">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




