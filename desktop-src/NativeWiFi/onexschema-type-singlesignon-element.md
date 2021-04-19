---
description: 指定何時執行單一登入。
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: 輸入 (singleSignOn) 元素
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
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970210"
---
# <a name="type-singlesignon-element"></a><span data-ttu-id="b1d4a-103">輸入 (singleSignOn) 元素</span><span class="sxs-lookup"><span data-stu-id="b1d4a-103">type (singleSignOn) Element</span></span>

<span data-ttu-id="b1d4a-104">類型 (singleSignOn) 元素會指定何時執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="b1d4a-104">The type (singleSignOn) element specifies when single sign on is performed.</span></span> <span data-ttu-id="b1d4a-105">當設定為時 `preLogon` ，會在使用者登入之前執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="b1d4a-105">When set to `preLogon`, single sign on is performed before the user logs on.</span></span> <span data-ttu-id="b1d4a-106">當設定為時 `postLogon` ，會在使用者登入後立即執行單一登入。</span><span class="sxs-lookup"><span data-stu-id="b1d4a-106">When set to `postLogon`, single sign on is performed immediately after the user logs on.</span></span>

<span data-ttu-id="b1d4a-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="b1d4a-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b1d4a-108">**Type** 元素是由 [**singleSignOn**](onexschema-singlesignon-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="b1d4a-108">The **type** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d4a-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1d4a-109">Requirements</span></span>



| <span data-ttu-id="b1d4a-110">需求</span><span class="sxs-lookup"><span data-stu-id="b1d4a-110">Requirement</span></span> | <span data-ttu-id="b1d4a-111">值</span><span class="sxs-lookup"><span data-stu-id="b1d4a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1d4a-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1d4a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d4a-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1d4a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b1d4a-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1d4a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d4a-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1d4a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1d4a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1d4a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1d4a-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b1d4a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b1d4a-118">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="b1d4a-118">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="b1d4a-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b1d4a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b1d4a-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="b1d4a-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




