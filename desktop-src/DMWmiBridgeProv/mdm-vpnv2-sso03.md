---
title: MDM_VPNv2_Sso03 類別
description: 在 \_ \_ 裝置合規性的情況下，您可以使用 MDM >vpnv2 Sso03 類別來選取與 VPN 驗證憑證不同的憑證來進行 Kerberos 驗證。
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- MDM_VPNv2_Sso03 類別
- MDM_VPNv2_Sso03 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50661abb26bc84aa9db09771a16d254c0b97fa183550315cb170688c15a3a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833798"
---
# <a name="mdm_vpnv2_sso03-class"></a>MDM \_ >vpnv2 \_ Sso03 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

在裝置合規性的情況下，您可以使用 **MDM \_ >vpnv2 \_ Sso03** 類別來選取與 VPN 驗證憑證不同的憑證來進行 Kerberos 驗證。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a>成員

**MDM \_ >vpnv2 \_ Sso03** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ >vpnv2 \_ Sso03** 類別具有這些屬性。

<dl> <dt>

[Eku](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[Enabled](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
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

[IssuerHash](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

資料類型： **字串**
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

描述父節點的完整路徑。 針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"

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

 

