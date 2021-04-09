---
description: 表示網路的操作模式。
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: connectionType (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1e7b456260c656ebb3d64b6a3732fe97ca3ca488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848406"
---
# <a name="connectiontype-wlanprofile-element"></a><span data-ttu-id="b757d-103">connectionType (WLANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="b757d-103">connectionType (WLANProfile) Element</span></span>

<span data-ttu-id="b757d-104">ConnectionType (WLANProfile) 元素指出網路的作業模式。</span><span class="sxs-lookup"><span data-stu-id="b757d-104">The connectionType (WLANProfile) element indicates the operating mode of the network.</span></span>

<span data-ttu-id="b757d-105">**ESS** 的值表示基礎結構網路，而 **IBSS** 則表示臨機操作網路。</span><span class="sxs-lookup"><span data-stu-id="b757d-105">A value of **ESS** indicates an infrastructure network, while **IBSS** indicates an ad-hoc network.</span></span>

``` syntax
<xs:element name="connectionType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="IBSS"
             />
            <xs:enumeration
                value="ESS"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b757d-106">**ConnectionType** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="b757d-106">The **connectionType** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="b757d-107">範例</span><span class="sxs-lookup"><span data-stu-id="b757d-107">Examples</span></span>

<span data-ttu-id="b757d-108">若要查看使用 **connectionType** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="b757d-108">To view sample profiles that use the **connectionType** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b757d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="b757d-109">Requirements</span></span>



| <span data-ttu-id="b757d-110">需求</span><span class="sxs-lookup"><span data-stu-id="b757d-110">Requirement</span></span> | <span data-ttu-id="b757d-111">值</span><span class="sxs-lookup"><span data-stu-id="b757d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b757d-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b757d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b757d-113">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b757d-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b757d-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b757d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b757d-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b757d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b757d-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b757d-116">Redistributable</span></span><br/>          | <span data-ttu-id="b757d-117">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="b757d-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b757d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b757d-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="b757d-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b757d-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b757d-120">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="b757d-120">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="b757d-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b757d-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b757d-122">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="b757d-122">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




