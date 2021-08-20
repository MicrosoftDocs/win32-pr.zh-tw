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
ms.openlocfilehash: faf6f775acac44af3f591dbcea0b32dd70d9ec80bb479c9d05145aee13d544a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984998"
---
# <a name="dot11_phy_type-enumeration"></a>DOT11 \_ PHY \_ 類型列舉

**DOT11 \_ phy \_ 型** 別列舉定義了 802.11 phy 和媒體類型。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11 \_ phy \_ 類型 \_ 不明**
</dt> <dd>

指定未知或未初始化的 PHY 類型。

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11 \_ phy \_ 類型 \_ any**
</dt> <dd>

指定任何 PHY 類型。

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11 \_ phy \_ 類型 \_ fhss**
</dt> <dd>

指定頻率跳動頻外 (FHSS) PHY。 藍牙的裝置可以使用 FHSS 或 FHSS 的調適。

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11 \_ phy \_ 類型 \_ dsss**
</dt> <dd>

指定直接序列分散頻譜 (DSSS) PHY 類型。

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11 \_ phy \_ 類型 \_ irbaseband**
</dt> <dd>

指定紅外線 (IR) 基帶 PHY 類型。

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11 \_ phy \_ 類型 \_ ofdm**
</dt> <dd>

指定 (OFDM) PHY 類型的正向頻率除法多工。 802.11 a 裝置可以使用 OFDM。

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11 \_ phy \_ 類型 \_ hrdsss**
</dt> <dd>

指定高比率的 DSSS (HRDSSS) PHY 類型。

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11 \_ phy \_ 類型 \_ erp**
</dt> <dd>

指定 (ERP) 的擴充速率 PHY 類型。 802.11 g 裝置可以使用 ERP。

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11 \_ phy \_ 類型 \_ ht**
</dt> <dd>

指定 802.11 n PHY 類型。

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11 \_ phy \_ 類型 \_ vht**
</dt> <dd>

指定 802.11 ac PHY 類型。 這是 IEEE 802.11 ac 中指定的高輸送量 PHY 類型。

Windows 8.1、Windows Server 2012 R2 和更新版本都支援此值。

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11 \_ phy \_ 類型 \_ IHV \_ 開始**
</dt> <dd>

指定範圍的開頭，此範圍用來定義獨立硬體廠商 (IHV) 所開發的 PHY 類型。

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11 \_ phy \_ type \_ IHV \_ end**
</dt> <dd>

指定範圍的開頭，此範圍用來定義獨立硬體廠商 (IHV) 所開發的 PHY 類型。

</dd> </dl>

## <a name="remarks"></a>備註

IHV 可以從 **dot11 \_ phy \_ type \_ ihv \_ 開始** 至 **dot11 \_ PHY \_ type \_ ihv \_ end**，指派其專屬 PHY 類型的值。 IHV 必須為每個專屬的 PHY 類型指派此範圍內的唯一數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Windot11。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WLAN \_ 關聯 \_ 屬性**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**WLAN \_ 介面 \_ 功能**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




