---
description: 指定 IHV 安全性元件所使用之 802.1 X 安全性設定的來源。
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: useMSOneX (IHV) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944470"
---
# <a name="usemsonex-ihv-element"></a><span data-ttu-id="fe12c-103">useMSOneX (IHV) 元素</span><span class="sxs-lookup"><span data-stu-id="fe12c-103">useMSOneX (IHV) Element</span></span>

<span data-ttu-id="fe12c-104">**UseMSOneX** (ihv) 元素會指定 IHV 安全性元件所使用的 802.1 x 安全性設定來源。</span><span class="sxs-lookup"><span data-stu-id="fe12c-104">The **useMSOneX** (IHV) element specifies the origin of 802.1X security settings used by an IHV security component.</span></span>

<span data-ttu-id="fe12c-105">當 **useMSOneX** 為 true 時，IHV 安全性元件會使用 Microsoft 定義的 802.1 x 設定。</span><span class="sxs-lookup"><span data-stu-id="fe12c-105">When **useMSOneX** is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="fe12c-106">當 **useMSOneX** 為 false 時，IHV 安全性元件會使用廠商提供的 802.1 x 設定。</span><span class="sxs-lookup"><span data-stu-id="fe12c-106">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span>

<span data-ttu-id="fe12c-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="fe12c-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="fe12c-108">元素是由 [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) 元素定義。</span><span class="sxs-lookup"><span data-stu-id="fe12c-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe12c-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe12c-109">Requirements</span></span>



| <span data-ttu-id="fe12c-110">需求</span><span class="sxs-lookup"><span data-stu-id="fe12c-110">Requirement</span></span> | <span data-ttu-id="fe12c-111">值</span><span class="sxs-lookup"><span data-stu-id="fe12c-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe12c-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe12c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fe12c-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe12c-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fe12c-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe12c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fe12c-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe12c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe12c-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe12c-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe12c-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="fe12c-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fe12c-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="fe12c-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="fe12c-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="fe12c-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fe12c-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="fe12c-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




