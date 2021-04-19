---
description: 指定在驗證嘗試失敗之後，用戶端不會重新嘗試驗證的時間長度（以秒為單位）。
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: heldPeriod (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981560"
---
# <a name="heldperiod-onex-element"></a><span data-ttu-id="1603b-103">heldPeriod (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="1603b-103">heldPeriod (OneX) Element</span></span>

<span data-ttu-id="1603b-104">HeldPeriod (OneX) 元素會指定用戶端在驗證嘗試失敗之後不會重新嘗試驗證的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1603b-104">The heldPeriod (OneX) element specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span>

<span data-ttu-id="1603b-105">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="1603b-105">This element is optional.</span></span> <span data-ttu-id="1603b-106">當設定檔中未指定 heldPeriod 時，會使用1秒的值。</span><span class="sxs-lookup"><span data-stu-id="1603b-106">When heldPeriod is not specified in a profile, a value of 1 second is used.</span></span>

<span data-ttu-id="1603b-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="1603b-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="1603b-108">**HeldPeriod** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="1603b-108">The **heldPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1603b-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="1603b-109">Requirements</span></span>



| <span data-ttu-id="1603b-110">需求</span><span class="sxs-lookup"><span data-stu-id="1603b-110">Requirement</span></span> | <span data-ttu-id="1603b-111">值</span><span class="sxs-lookup"><span data-stu-id="1603b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1603b-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1603b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1603b-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1603b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1603b-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1603b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1603b-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1603b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1603b-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1603b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="1603b-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="1603b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1603b-118">**OneX**</span><span class="sxs-lookup"><span data-stu-id="1603b-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="1603b-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="1603b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1603b-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="1603b-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




