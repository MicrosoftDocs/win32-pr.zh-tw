---
title: IMsRdpClientAdvancedSettings7 NetworkConnectionType 屬性
description: 取得或設定用戶端與伺服器之間使用的網路連接類型。 傳遞至伺服器的網路連接類型資訊，可協助伺服器根據網路連線類型調整數個參數。
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- NetworkConnectionType 屬性遠端桌面服務
- NetworkConnectionType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，NetworkConnectionType 屬性
- NetworkConnectionType 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，NetworkConnectionType 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969179"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a><span data-ttu-id="5c787-109">IMsRdpClientAdvancedSettings7：： NetworkConnectionType 屬性</span><span class="sxs-lookup"><span data-stu-id="5c787-109">IMsRdpClientAdvancedSettings7::NetworkConnectionType property</span></span>

<span data-ttu-id="5c787-110">取得或設定用戶端與伺服器之間使用的網路連接類型。</span><span class="sxs-lookup"><span data-stu-id="5c787-110">Gets or sets the type of network connection used between the client and server.</span></span> <span data-ttu-id="5c787-111">傳遞至伺服器的網路連接類型資訊，可協助伺服器根據網路連線類型調整數個參數。</span><span class="sxs-lookup"><span data-stu-id="5c787-111">The network connection type information passed on to the server helps the server tune several parameters based on the network connection type.</span></span>

<span data-ttu-id="5c787-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5c787-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c787-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c787-113">Syntax</span></span>


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a><span data-ttu-id="5c787-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="5c787-114">Property value</span></span>

<span data-ttu-id="5c787-115">網路連接類型。</span><span class="sxs-lookup"><span data-stu-id="5c787-115">The network connection type.</span></span>

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span data-ttu-id="5c787-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**連接 \_輸入 \_ 數據機** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="5c787-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION\_TYPE\_MODEM** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5c787-117">數據機 (56 Kbps) </span><span class="sxs-lookup"><span data-stu-id="5c787-117">Modem (56 Kbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span data-ttu-id="5c787-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**連接 \_輸入 \_ 寬頻 \_ 低** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="5c787-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION\_TYPE\_BROADBAND\_LOW** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="5c787-119">低速度寬頻 (256 Kbps 到 2 Mbps) </span><span class="sxs-lookup"><span data-stu-id="5c787-119">Low-speed broadband (256 Kbps to 2 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span data-ttu-id="5c787-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**連接 \_輸入 \_ 衛星** (3 (0x3) ) </span><span class="sxs-lookup"><span data-stu-id="5c787-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION\_TYPE\_SATELLITE** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="5c787-121">附屬 (2 Mbps 至 16 Mbps，具有高延遲) </span><span class="sxs-lookup"><span data-stu-id="5c787-121">Satellite (2 Mbps to 16 Mbps, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span data-ttu-id="5c787-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**連接 \_輸入 \_ 寬頻 \_ HIGH** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="5c787-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION\_TYPE\_BROADBAND\_HIGH** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="5c787-123">高速寬頻 (2 Mbps 至 10 Mbps) </span><span class="sxs-lookup"><span data-stu-id="5c787-123">High-speed broadband (2 Mbps to 10 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span data-ttu-id="5c787-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**連接 \_輸入 \_ WAN** (5 (0x5) ) </span><span class="sxs-lookup"><span data-stu-id="5c787-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION\_TYPE\_WAN** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="5c787-125">廣域網路 (WAN)  (10 Mbps 或更高，且具有高延遲) </span><span class="sxs-lookup"><span data-stu-id="5c787-125">Wide area network (WAN) (10 Mbps or higher, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span data-ttu-id="5c787-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**連接 \_輸入 \_ LAN** (6 (0x6) ) </span><span class="sxs-lookup"><span data-stu-id="5c787-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION\_TYPE\_LAN** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="5c787-127">區域網路 (LAN)  (10 Mbps 或更高版本) </span><span class="sxs-lookup"><span data-stu-id="5c787-127">Local area network (LAN) (10 Mbps or higher)</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c787-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c787-128">Requirements</span></span>



| <span data-ttu-id="5c787-129">需求</span><span class="sxs-lookup"><span data-stu-id="5c787-129">Requirement</span></span> | <span data-ttu-id="5c787-130">值</span><span class="sxs-lookup"><span data-stu-id="5c787-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c787-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c787-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5c787-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c787-132">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="5c787-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c787-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5c787-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c787-134">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="5c787-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5c787-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c787-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c787-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5c787-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5c787-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c787-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c787-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5c787-139">IID</span><span class="sxs-lookup"><span data-stu-id="5c787-139">IID</span></span><br/>                      | <span data-ttu-id="5c787-140">IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="5c787-140">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c787-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c787-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c787-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5c787-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5c787-143">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5c787-143">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





