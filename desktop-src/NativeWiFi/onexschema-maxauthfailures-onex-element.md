---
description: 指定一組認證允許的驗證失敗次數上限。
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: maxAuthFailures (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513348"
---
# <a name="maxauthfailures-onex-element"></a><span data-ttu-id="e454e-103">maxAuthFailures (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="e454e-103">maxAuthFailures (OneX) Element</span></span>

<span data-ttu-id="e454e-104">MaxAuthFailures (OneX) 元素會指定一組認證所允許的驗證失敗次數上限。</span><span class="sxs-lookup"><span data-stu-id="e454e-104">The maxAuthFailures (OneX) element specifies the maximum number of authentication failures allowed for a set of credentials.</span></span>

<span data-ttu-id="e454e-105">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="e454e-105">This element is optional.</span></span> <span data-ttu-id="e454e-106">當設定檔中未指定 maxAuthFailures 時，會使用一個值。</span><span class="sxs-lookup"><span data-stu-id="e454e-106">When maxAuthFailures is not specified in a profile, a value of one is used.</span></span>

<span data-ttu-id="e454e-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="e454e-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="e454e-108">**MaxAuthFailures** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="e454e-108">The **maxAuthFailures** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e454e-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="e454e-109">Requirements</span></span>



| <span data-ttu-id="e454e-110">需求</span><span class="sxs-lookup"><span data-stu-id="e454e-110">Requirement</span></span> | <span data-ttu-id="e454e-111">值</span><span class="sxs-lookup"><span data-stu-id="e454e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e454e-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e454e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e454e-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e454e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e454e-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e454e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e454e-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e454e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e454e-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e454e-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="e454e-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e454e-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e454e-118">**OneX**</span><span class="sxs-lookup"><span data-stu-id="e454e-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="e454e-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e454e-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e454e-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="e454e-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




