---
description: 包含無線局域網路設定檔的名稱。
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: WLANProfile) 專案的名稱 (
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512520"
---
# <a name="name-wlanprofile-element"></a><span data-ttu-id="ae617-103">WLANProfile) 專案的名稱 (</span><span class="sxs-lookup"><span data-stu-id="ae617-103">name (WLANProfile) Element</span></span>

<span data-ttu-id="ae617-104">名稱 (WLANProfile) 元素包含無線局域網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae617-104">The name (WLANProfile) element contains the name of a wireless LAN profile.</span></span>

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

<span data-ttu-id="ae617-105">**Name** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="ae617-105">The **name** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae617-106">備註</span><span class="sxs-lookup"><span data-stu-id="ae617-106">Remarks</span></span>

<span data-ttu-id="ae617-107">名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ae617-107">Names are case-sensitive.</span></span>

<span data-ttu-id="ae617-108">若為 Windows XP Service Pack 3 (SP3) 和適用于 Windows XP Service Pack 2 (SP2) 的無線區域網路 API，當設定檔儲存在設定檔存放區時，就會忽略 name 元素。</span><span class="sxs-lookup"><span data-stu-id="ae617-108">For Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2), the name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="ae617-109">設定檔的名稱衍生自網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="ae617-109">The name of the profile is derived from the SSID of the network.</span></span> <span data-ttu-id="ae617-110">在基礎結構網路設定檔中，設定檔的名稱是網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="ae617-110">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="ae617-111">針對臨機操作網路設定檔，設定檔的名稱是臨機操作網路的 SSID，後面接著 `-adhoc` 。</span><span class="sxs-lookup"><span data-stu-id="ae617-111">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> <span data-ttu-id="ae617-112">XML escape 字元（例如 &）不會顯示。</span><span class="sxs-lookup"><span data-stu-id="ae617-112">XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="ae617-113">針對 windows XP 加裝 SP3 或適用于 Windows XP SP2 的無線區域網路 API 所部署的設定檔，請避免在 SSID 名稱中使用 XML escape 字元。</span><span class="sxs-lookup"><span data-stu-id="ae617-113">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 or Wireless LAN API for Windows XP with SP2.</span></span>

<span data-ttu-id="ae617-114">對於任何僅適用于 Windows Vista 或 Windows Server 2008 的網路設定檔，其名稱可以是任何字串。</span><span class="sxs-lookup"><span data-stu-id="ae617-114">For any network profile intended for use only on Windows Vista or Windows Server 2008, the name can be any string.</span></span>

## <a name="examples"></a><span data-ttu-id="ae617-115">範例</span><span class="sxs-lookup"><span data-stu-id="ae617-115">Examples</span></span>

<span data-ttu-id="ae617-116">若要查看使用 **name** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="ae617-116">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae617-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae617-117">Requirements</span></span>



| <span data-ttu-id="ae617-118">需求</span><span class="sxs-lookup"><span data-stu-id="ae617-118">Requirement</span></span> | <span data-ttu-id="ae617-119">值</span><span class="sxs-lookup"><span data-stu-id="ae617-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ae617-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae617-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae617-121">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae617-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ae617-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae617-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae617-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae617-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ae617-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ae617-124">Redistributable</span></span><br/>          | <span data-ttu-id="ae617-125">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="ae617-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ae617-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae617-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae617-127">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="ae617-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ae617-128">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="ae617-128">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ae617-129">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="ae617-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ae617-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="ae617-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




