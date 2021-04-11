---
description: 指定單一登入連接嘗試失敗之前的延遲上限（以秒為單位）。
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: maxDelay (singleSignOn) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849138"
---
# <a name="maxdelay-singlesignon-element"></a><span data-ttu-id="b39ad-103">maxDelay (singleSignOn) 元素</span><span class="sxs-lookup"><span data-stu-id="b39ad-103">maxDelay (singleSignOn) Element</span></span>

<span data-ttu-id="b39ad-104">MaxDelay (singleSignOn) 元素會指定單一登入連接嘗試失敗之前的延遲上限（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b39ad-104">The maxDelay (singleSignOn) element specifies, in seconds, the maximum delay before the single sign on connection attempt fails.</span></span>

<span data-ttu-id="b39ad-105">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="b39ad-105">This element is optional.</span></span> <span data-ttu-id="b39ad-106">當設定檔中未指定 maxDelay 時，會使用10秒的值。</span><span class="sxs-lookup"><span data-stu-id="b39ad-106">When maxDelay is not specified in a profile, a value of 10 seconds is used.</span></span>

<span data-ttu-id="b39ad-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="b39ad-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b39ad-108">**MaxDelay** 元素是由 [**singleSignOn**](onexschema-singlesignon-onex-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="b39ad-108">The **maxDelay** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b39ad-109">備註</span><span class="sxs-lookup"><span data-stu-id="b39ad-109">Remarks</span></span>

<span data-ttu-id="b39ad-110">您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。</span><span class="sxs-lookup"><span data-stu-id="b39ad-110">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="b39ad-111">如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="b39ad-111">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b39ad-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b39ad-112">Requirements</span></span>



| <span data-ttu-id="b39ad-113">需求</span><span class="sxs-lookup"><span data-stu-id="b39ad-113">Requirement</span></span> | <span data-ttu-id="b39ad-114">值</span><span class="sxs-lookup"><span data-stu-id="b39ad-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b39ad-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b39ad-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b39ad-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b39ad-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b39ad-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b39ad-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b39ad-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b39ad-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b39ad-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b39ad-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="b39ad-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b39ad-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b39ad-121">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="b39ad-121">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="b39ad-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b39ad-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b39ad-123">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="b39ad-123">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
