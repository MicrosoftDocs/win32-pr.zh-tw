---
title: MDM_VPNv2_RouteList02_01 類別
description: MDM \_ >vpnv2 \_ RouteList02 \_ 01 類別包含要新增至 VPN 介面路由表的選擇性路由清單。
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01 類別
- MDM_VPNv2_RouteList02_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ea9725d70d3acfe4e6831d1d386aedecfd9374728b103d50b67aa15cb61ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750268"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>MDM \_ >vpnv2 \_ RouteList02 \_ 01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ >vpnv2 \_ RouteList02 \_ 01** 類別包含要新增至 VPN 介面路由表的選擇性路由清單。

這是分割通道案例的必要項，其中 VPN 伺服器網站有更多子網，預設子網是根據指派給介面的 IP。

執行 TCP/IP 的每部電腦都要決定其路由。 這些決定由 IP 路由表控制。 在此節點下新增值，就會使用 VPN 介面後置連線的路由來更新路由表。 此節點下的值代表 IP 路由的目的地前置詞。 目的地首碼包含 IP 位址首碼和前置長度。

在這裡新增路由，可讓網路堆疊識別需要透過 VPN 介面進行分割通道 VPN 的流量。 某些 VPN 伺服器可以在連線協商期間進行這項設定，而且在 VPN 設定檔中不需要這項資訊。 請洽詢您的 VPN 伺服器系統管理員，以判斷您是否需要在 VPN 設定檔中使用這項資訊。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a>成員

**MDM \_ >vpnv2 \_ RouteList02 \_ 01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ >vpnv2 \_ RouteList02 \_ 01** 類別具有這些屬性。

<dl> <dt>

[位址](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"

</dd> <dt>

[PrefixSize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

