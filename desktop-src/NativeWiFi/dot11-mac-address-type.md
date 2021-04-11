---
description: 用來定義 IEEE 媒體存取控制 (MAC) 位址。
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: 'DOT11_MAC_ADDRESS (Windot11) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849924"
---
# <a name="dot11_mac_address"></a><span data-ttu-id="ea525-103">DOT11 \_ MAC \_ 位址</span><span class="sxs-lookup"><span data-stu-id="ea525-103">DOT11\_MAC\_ADDRESS</span></span>

<span data-ttu-id="ea525-104">**DOT11 \_ mac \_ 位址** 類型可用來定義 IEEE 媒體存取控制 (mac) 位址。</span><span class="sxs-lookup"><span data-stu-id="ea525-104">The **DOT11\_MAC\_ADDRESS** types are used to define an IEEE media access control (MAC) address.</span></span>


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="ea525-105">**DOT11 \_ MAC \_ 位址 \[ 6\]**</span><span class="sxs-lookup"><span data-stu-id="ea525-105">**DOT11\_MAC\_ADDRESS\[6\]**</span></span>
</dt> <dd>

<span data-ttu-id="ea525-106">單播、多播或廣播格式的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="ea525-106">A MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> <dt>

<span data-ttu-id="ea525-107">**PDOT11 \_ MAC \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="ea525-107">**PDOT11\_MAC\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="ea525-108">單播、多播或廣播格式的 MAC 位址指標。</span><span class="sxs-lookup"><span data-stu-id="ea525-108">Pointer to a MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea525-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea525-109">Requirements</span></span>



| <span data-ttu-id="ea525-110">需求</span><span class="sxs-lookup"><span data-stu-id="ea525-110">Requirement</span></span> | <span data-ttu-id="ea525-111">值</span><span class="sxs-lookup"><span data-stu-id="ea525-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea525-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea525-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ea525-113">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea525-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea525-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea525-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ea525-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea525-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ea525-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ea525-116">Redistributable</span></span><br/>          | <span data-ttu-id="ea525-117">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="ea525-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="ea525-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ea525-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea525-119"><dt>Windot11 (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="ea525-119"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea525-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea525-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea525-121">**DOT11 \_ BSSID \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="ea525-121">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> <dt>

[<span data-ttu-id="ea525-122">**WLAN \_ 關聯 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="ea525-122">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="ea525-123">**WLAN \_ BSS \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="ea525-123">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




