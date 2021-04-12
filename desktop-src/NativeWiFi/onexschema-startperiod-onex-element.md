---
description: 指定傳送 EAPOL-Start 之前等候的時間長度（以秒為單位）。
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: startPeriod (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319115"
---
# <a name="startperiod-onex-element"></a><span data-ttu-id="416ca-103">startPeriod (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="416ca-103">startPeriod (OneX) Element</span></span>

<span data-ttu-id="416ca-104">StartPeriod (OneX) 元素會指定傳送 EAPOL-Start 之前等候的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="416ca-104">The startPeriod (OneX) element specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="416ca-105">傳送 EAPOL-Start 訊息以啟動 802.1 X 驗證程式。</span><span class="sxs-lookup"><span data-stu-id="416ca-105">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span>

<span data-ttu-id="416ca-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="416ca-106">This element is optional.</span></span> <span data-ttu-id="416ca-107">當設定檔中未指定 startPeriod 時，會使用值5秒。</span><span class="sxs-lookup"><span data-stu-id="416ca-107">When startPeriod is not specified in a profile, a value of 5 seconds is used.</span></span>

<span data-ttu-id="416ca-108">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="416ca-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="startPeriod">
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

<span data-ttu-id="416ca-109">**StartPeriod** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="416ca-109">The **startPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="416ca-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="416ca-110">Requirements</span></span>



| <span data-ttu-id="416ca-111">需求</span><span class="sxs-lookup"><span data-stu-id="416ca-111">Requirement</span></span> | <span data-ttu-id="416ca-112">值</span><span class="sxs-lookup"><span data-stu-id="416ca-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="416ca-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="416ca-113">Minimum supported client</span></span><br/> | <span data-ttu-id="416ca-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="416ca-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="416ca-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="416ca-115">Minimum supported server</span></span><br/> | <span data-ttu-id="416ca-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="416ca-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="416ca-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="416ca-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="416ca-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="416ca-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="416ca-119">**OneX**</span><span class="sxs-lookup"><span data-stu-id="416ca-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="416ca-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="416ca-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="416ca-121">**OneX**</span><span class="sxs-lookup"><span data-stu-id="416ca-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




