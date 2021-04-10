---
description: 指定用戶端等候驗證器回應的最大時間長度（以秒為單位）。
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: authPeriod (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026718"
---
# <a name="authperiod-onex-element"></a><span data-ttu-id="db8c2-103">authPeriod (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="db8c2-103">authPeriod (OneX) Element</span></span>

<span data-ttu-id="db8c2-104">AuthPeriod (OneX) 元素會指定用戶端等待驗證器回應的最大時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="db8c2-104">The authPeriod (OneX) element specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="db8c2-105">如果在指定的期間內未收到回應，用戶端會假設網路上沒有任何驗證器存在。</span><span class="sxs-lookup"><span data-stu-id="db8c2-105">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="db8c2-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="db8c2-106">This element is optional.</span></span> <span data-ttu-id="db8c2-107">當設定檔中未指定 authPeriod 時，會使用值18秒。</span><span class="sxs-lookup"><span data-stu-id="db8c2-107">When authPeriod is not specified in a profile, a value of 18 seconds is used.</span></span>

<span data-ttu-id="db8c2-108">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="db8c2-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authPeriod">
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

<span data-ttu-id="db8c2-109">**AuthPeriod** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="db8c2-109">The **authPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="db8c2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="db8c2-110">Requirements</span></span>



| <span data-ttu-id="db8c2-111">需求</span><span class="sxs-lookup"><span data-stu-id="db8c2-111">Requirement</span></span> | <span data-ttu-id="db8c2-112">值</span><span class="sxs-lookup"><span data-stu-id="db8c2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db8c2-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db8c2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="db8c2-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db8c2-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db8c2-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db8c2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="db8c2-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db8c2-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db8c2-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db8c2-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="db8c2-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="db8c2-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="db8c2-119">**OneX**</span><span class="sxs-lookup"><span data-stu-id="db8c2-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="db8c2-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="db8c2-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="db8c2-121">**OneX**</span><span class="sxs-lookup"><span data-stu-id="db8c2-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




