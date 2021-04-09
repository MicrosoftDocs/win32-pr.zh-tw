---
description: 包含介面的 SSID。
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: 'DOT11_SSID 結構 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849916"
---
# <a name="dot11_ssid-structure"></a><span data-ttu-id="ec20e-103">DOT11 \_ SSID 結構</span><span class="sxs-lookup"><span data-stu-id="ec20e-103">DOT11\_SSID structure</span></span>

<span data-ttu-id="ec20e-104">**DOT11 \_ ssid** 結構包含介面的 ssid。</span><span class="sxs-lookup"><span data-stu-id="ec20e-104">A **DOT11\_SSID** structure contains the SSID of an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec20e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec20e-105">Syntax</span></span>


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a><span data-ttu-id="ec20e-106">成員</span><span class="sxs-lookup"><span data-stu-id="ec20e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec20e-107">**uSSIDLength**</span><span class="sxs-lookup"><span data-stu-id="ec20e-107">**uSSIDLength**</span></span>
</dt> <dd>

<span data-ttu-id="ec20e-108">**UcSSID** 陣列的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ec20e-108">The length, in bytes, of the **ucSSID** array.</span></span>

</dd> <dt>

<span data-ttu-id="ec20e-109">**ucSSID**</span><span class="sxs-lookup"><span data-stu-id="ec20e-109">**ucSSID**</span></span>
</dt> <dd>

<span data-ttu-id="ec20e-110">SSID。</span><span class="sxs-lookup"><span data-stu-id="ec20e-110">The SSID.</span></span> <span data-ttu-id="ec20e-111">DOT11 \_ SSID \_ 最大 \_ 長度設為32。</span><span class="sxs-lookup"><span data-stu-id="ec20e-111">DOT11\_SSID\_MAX\_LENGTH is set to 32.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec20e-112">備註</span><span class="sxs-lookup"><span data-stu-id="ec20e-112">Remarks</span></span>

<span data-ttu-id="ec20e-113">**UcSSID** 成員所指定的 SSID 不是以 null 結束的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="ec20e-113">The SSID that is specified by the **ucSSID** member is not a null-terminated ASCII string.</span></span> <span data-ttu-id="ec20e-114">SSID 的長度取決於 **uSSIDLength** 成員。</span><span class="sxs-lookup"><span data-stu-id="ec20e-114">The length of the SSID is determined by the **uSSIDLength** member.</span></span>

<span data-ttu-id="ec20e-115">萬用字元 SSID 是其 **uSSIDLength** 成員設定為零的 ssid。</span><span class="sxs-lookup"><span data-stu-id="ec20e-115">A wildcard SSID is an SSID whose **uSSIDLength** member is set to zero.</span></span> <span data-ttu-id="ec20e-116">當所需的 SSID 設定為萬用字元 SSID 時，802.11 工作站可以連接到任何基本的服務集 (BSS) 網路。</span><span class="sxs-lookup"><span data-stu-id="ec20e-116">When the desired SSID is set to the wildcard SSID, the 802.11 station can connect to any basic service set (BSS) network.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec20e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec20e-117">Requirements</span></span>



| <span data-ttu-id="ec20e-118">需求</span><span class="sxs-lookup"><span data-stu-id="ec20e-118">Requirement</span></span> | <span data-ttu-id="ec20e-119">值</span><span class="sxs-lookup"><span data-stu-id="ec20e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec20e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec20e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ec20e-121">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec20e-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ec20e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec20e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ec20e-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec20e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ec20e-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ec20e-124">Redistributable</span></span><br/>          | <span data-ttu-id="ec20e-125">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="ec20e-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="ec20e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ec20e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec20e-127"><dt>Wlantypes (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="ec20e-127"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec20e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec20e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec20e-129">**WLAN \_ 連接 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="ec20e-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="ec20e-130">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="ec20e-130">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[<span data-ttu-id="ec20e-131">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="ec20e-131">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




