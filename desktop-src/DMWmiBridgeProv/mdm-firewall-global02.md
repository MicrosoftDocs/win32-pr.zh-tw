---
title: MDM_Firewall_Global02 類別
description: MDM \_ 防火牆 \_ Global02 類別可用來設定 Windows Defender 防火牆設定。
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- MDM_Firewall_Global02 類別
- MDM_Firewall_Global02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020cec92aba6c8acf01f33952364bce6c8ef2027be49e2b9061f97d74e8f8bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165821"
---
# <a name="mdm_firewall_global02-class"></a>MDM \_ 防火牆 \_ Global02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

MDM \_ 防火牆 \_ Global02 類別可用來設定 Windows Defender 防火牆設定。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a>成員

**MDM \_ 防火牆 \_ Global02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ 防火牆 \_ Global02** 類別具有這些屬性。

<dl> <dt>

[BinaryVersionSupported](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[CRLcheck](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[CurrentProfiles](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DisableStatefulFtp](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[EnablePacketQueue](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
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

</dd> <dt>

[IPsecExempt](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[OpportunisticallyMatchAuthSetPerKM](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
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

</dd> <dt>

[PolicyVersion](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[PolicyVersionSupported](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[PresharedKeyEncoding](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[SaIdleTime](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

