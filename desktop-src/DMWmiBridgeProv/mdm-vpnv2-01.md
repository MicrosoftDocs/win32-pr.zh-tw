---
title: MDM_VPNv2_01 類別
description: MDM \_ >vpnv2 \_ 01 類別允許設定裝置的 VPN 設定檔。
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- MDM_VPNv2_01 類別
- MDM_VPNv2_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7580d3592f1479475bf93d899a35864c0ca95ef36fa01fc9c5b07bc284395773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693428"
---
# <a name="mdm_vpnv2_01-class"></a>MDM \_ >vpnv2 \_ 01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ >vpnv2 \_ 01** 類別允許設定裝置的 VPN 設定檔。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a>成員

**MDM \_ >vpnv2 \_ 01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ >vpnv2 \_ 01** 類別具有這些屬性。

<dl> <dt>

[AlwaysOn](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[ByPassForLocal](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DnsSuffix](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[EdpModeId](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
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

識別父節點的名稱。 針對此類別，此字串為 VPN 設定檔名稱。

</dd> <dt>

[LockDown](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/VPNv2"

</dd> <dt>

[ProfileXML](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[RememberCredentials](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[TrustedNetworkDetection](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

