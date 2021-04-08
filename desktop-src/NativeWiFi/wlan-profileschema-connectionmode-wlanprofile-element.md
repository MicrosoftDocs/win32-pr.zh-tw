---
description: 指出無線區域網路的連接是否應該自動或由使用者起始。
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: connectionMode (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691555"
---
# <a name="connectionmode-wlanprofile-element"></a><span data-ttu-id="ae0e1-103">connectionMode (WLANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="ae0e1-103">connectionMode (WLANProfile) Element</span></span>

<span data-ttu-id="ae0e1-104">ConnectionMode (WLANProfile) 元素表示無線區域網路的連接是否應該自動或由使用者起始。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-104">The connectionMode (WLANProfile) element indicates whether connection to a wireless LAN should be automatic or initiated by user.</span></span>

<span data-ttu-id="ae0e1-105">如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 ESS，此值可以是 auto 或 manual。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-105">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either auto or manual.</span></span> <span data-ttu-id="ae0e1-106">如果這個元素不存在，則預設值為 auto。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-106">The default value is auto if this element is absent.</span></span>

<span data-ttu-id="ae0e1-107">如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 IBSS，則這個值必須是手動。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be manual.</span></span>

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ae0e1-108">**ConnectionMode** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-108">The **connectionMode** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae0e1-109">備註</span><span class="sxs-lookup"><span data-stu-id="ae0e1-109">Remarks</span></span>

<span data-ttu-id="ae0e1-110">下表描述列舉值。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-110">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="ae0e1-111">值</span><span class="sxs-lookup"><span data-stu-id="ae0e1-111">Value</span></span>  | <span data-ttu-id="ae0e1-112">描述</span><span class="sxs-lookup"><span data-stu-id="ae0e1-112">Description</span></span>                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae0e1-113">自動</span><span class="sxs-lookup"><span data-stu-id="ae0e1-113">auto</span></span>   | <span data-ttu-id="ae0e1-114">只要網路在範圍內，就應該自動起始無線網路的連接。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-114">The connection to the wireless network should be initiated automatically whenever the network is in range.</span></span> |
| <span data-ttu-id="ae0e1-115">manual</span><span class="sxs-lookup"><span data-stu-id="ae0e1-115">manual</span></span> | <span data-ttu-id="ae0e1-116">只有在使用者明確要求時，才會初始化無線網路的連接。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-116">The connection to the wireless network is only initated upon the explicit request of a user.</span></span>               |



 

## <a name="examples"></a><span data-ttu-id="ae0e1-117">範例</span><span class="sxs-lookup"><span data-stu-id="ae0e1-117">Examples</span></span>

<span data-ttu-id="ae0e1-118">若要查看使用 **connectionMode** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="ae0e1-118">To view sample profiles that use the **connectionMode** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae0e1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae0e1-119">Requirements</span></span>



| <span data-ttu-id="ae0e1-120">需求</span><span class="sxs-lookup"><span data-stu-id="ae0e1-120">Requirement</span></span> | <span data-ttu-id="ae0e1-121">值</span><span class="sxs-lookup"><span data-stu-id="ae0e1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ae0e1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae0e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae0e1-123">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae0e1-123">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ae0e1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae0e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae0e1-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae0e1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ae0e1-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ae0e1-126">Redistributable</span></span><br/>          | <span data-ttu-id="ae0e1-127">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="ae0e1-127">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ae0e1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae0e1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae0e1-129">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="ae0e1-129">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ae0e1-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="ae0e1-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ae0e1-131">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="ae0e1-131">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ae0e1-132">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="ae0e1-132">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




