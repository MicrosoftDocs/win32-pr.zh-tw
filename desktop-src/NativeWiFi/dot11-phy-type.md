---
description: 定義 802.11 PHY 和媒體類型。
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: 'DOT11_PHY_TYPE 列舉 (Windot11 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849920"
---
# <a name="dot11_phy_type-enumeration"></a><span data-ttu-id="23e60-103">DOT11 \_ PHY \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="23e60-103">DOT11\_PHY\_TYPE enumeration</span></span>

<span data-ttu-id="23e60-104">**DOT11 \_ phy \_ 型** 別列舉定義了 802.11 phy 和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-104">The **DOT11\_PHY\_TYPE** enumeration defines an 802.11 PHY and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e60-105">Syntax</span></span>


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="23e60-106">常數</span><span class="sxs-lookup"><span data-stu-id="23e60-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23e60-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11 \_ phy \_ 類型 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="23e60-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11\_phy\_type\_unknown**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-108">指定未知或未初始化的 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-108">Specifies an unknown or uninitialized PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11 \_ phy \_ 類型 \_ any**</span><span class="sxs-lookup"><span data-stu-id="23e60-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11\_phy\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-110">指定任何 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-110">Specifies any PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11 \_ phy \_ 類型 \_ fhss**</span><span class="sxs-lookup"><span data-stu-id="23e60-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11\_phy\_type\_fhss**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-112">指定頻率跳動頻外 (FHSS) PHY。</span><span class="sxs-lookup"><span data-stu-id="23e60-112">Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</span></span> <span data-ttu-id="23e60-113">藍牙裝置可以使用 FHSS 或 FHSS 調整。</span><span class="sxs-lookup"><span data-stu-id="23e60-113">Bluetooth devices can use FHSS or an adaptation of FHSS.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11 \_ phy \_ 類型 \_ dsss**</span><span class="sxs-lookup"><span data-stu-id="23e60-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11\_phy\_type\_dsss**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-115">指定直接序列分散頻譜 (DSSS) PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-115">Specifies a direct sequence spread spectrum (DSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11 \_ phy \_ 類型 \_ irbaseband**</span><span class="sxs-lookup"><span data-stu-id="23e60-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11\_phy\_type\_irbaseband**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-117">指定紅外線 (IR) 基帶 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-117">Specifies an infrared (IR) baseband PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11 \_ phy \_ 類型 \_ ofdm**</span><span class="sxs-lookup"><span data-stu-id="23e60-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11\_phy\_type\_ofdm**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-119">指定 (OFDM) PHY 類型的正向頻率除法多工。</span><span class="sxs-lookup"><span data-stu-id="23e60-119">Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.</span></span> <span data-ttu-id="23e60-120">802.11 a 裝置可以使用 OFDM。</span><span class="sxs-lookup"><span data-stu-id="23e60-120">802.11a devices can use OFDM.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11 \_ phy \_ 類型 \_ hrdsss**</span><span class="sxs-lookup"><span data-stu-id="23e60-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11\_phy\_type\_hrdsss**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-122">指定高比率的 DSSS (HRDSSS) PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-122">Specifies a high-rate DSSS (HRDSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11 \_ phy \_ 類型 \_ erp**</span><span class="sxs-lookup"><span data-stu-id="23e60-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11\_phy\_type\_erp**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-124">指定 (ERP) 的擴充速率 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-124">Specifies an extended rate PHY type (ERP).</span></span> <span data-ttu-id="23e60-125">802.11 g 裝置可以使用 ERP。</span><span class="sxs-lookup"><span data-stu-id="23e60-125">802.11g devices can use ERP.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11 \_ phy \_ 類型 \_ ht**</span><span class="sxs-lookup"><span data-stu-id="23e60-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11\_phy\_type\_ht**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-127">指定 802.11 n PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-127">Specifies the 802.11n PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11 \_ phy \_ 類型 \_ vht**</span><span class="sxs-lookup"><span data-stu-id="23e60-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11\_phy\_type\_vht**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-129">指定 802.11 ac PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-129">Specifies the 802.11ac PHY type.</span></span> <span data-ttu-id="23e60-130">這是 IEEE 802.11 ac 中指定的高輸送量 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-130">This is the very high throughput PHY type specified in IEEE 802.11ac.</span></span>

<span data-ttu-id="23e60-131">Windows 8.1、Windows Server 2012 R2 和更新版本都支援此值。</span><span class="sxs-lookup"><span data-stu-id="23e60-131">This value is supported on Windows 8.1, Windows Server 2012 R2, and later.</span></span>

</dd> <dt>

<span data-ttu-id="23e60-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11 \_ phy \_ 類型 \_ IHV \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="23e60-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11\_phy\_type\_IHV\_start**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-133">指定範圍的開頭，此範圍用來定義獨立硬體廠商 (IHV) 所開發的 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-133">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="23e60-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11 \_ phy \_ type \_ IHV \_ end**</span><span class="sxs-lookup"><span data-stu-id="23e60-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11\_phy\_type\_IHV\_end**</span></span>
</dt> <dd>

<span data-ttu-id="23e60-135">指定範圍的開頭，此範圍用來定義獨立硬體廠商 (IHV) 所開發的 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="23e60-135">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23e60-136">備註</span><span class="sxs-lookup"><span data-stu-id="23e60-136">Remarks</span></span>

<span data-ttu-id="23e60-137">IHV 可以從 **dot11 \_ phy \_ type \_ ihv \_ 開始** 至 **dot11 \_ PHY \_ type \_ ihv \_ end**，指派其專屬 PHY 類型的值。</span><span class="sxs-lookup"><span data-stu-id="23e60-137">An IHV can assign a value for its proprietary PHY types from **dot11\_phy\_type\_IHV\_start** through **dot11\_phy\_type\_IHV\_end**.</span></span> <span data-ttu-id="23e60-138">IHV 必須為每個專屬的 PHY 類型指派此範圍內的唯一數位。</span><span class="sxs-lookup"><span data-stu-id="23e60-138">The IHV must assign a unique number from this range for each of its proprietary PHY types.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e60-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="23e60-139">Requirements</span></span>



| <span data-ttu-id="23e60-140">需求</span><span class="sxs-lookup"><span data-stu-id="23e60-140">Requirement</span></span> | <span data-ttu-id="23e60-141">值</span><span class="sxs-lookup"><span data-stu-id="23e60-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23e60-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23e60-142">Minimum supported client</span></span><br/> | <span data-ttu-id="23e60-143">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23e60-143">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="23e60-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23e60-144">Minimum supported server</span></span><br/> | <span data-ttu-id="23e60-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23e60-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23e60-146">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="23e60-146">Redistributable</span></span><br/>          | <span data-ttu-id="23e60-147">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="23e60-147">Wireless LAN API for Windows XP with SP2</span></span><br/>                                   |
| <span data-ttu-id="23e60-148">標頭</span><span class="sxs-lookup"><span data-stu-id="23e60-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="23e60-149"><dt>Windot11。h</dt></span><span class="sxs-lookup"><span data-stu-id="23e60-149"><dt>Windot11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e60-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23e60-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e60-151">**WLAN \_ 關聯 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="23e60-151">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="23e60-152">**WLAN \_ 介面 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="23e60-152">**WLAN\_INTERFACE\_CAPABILITY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




