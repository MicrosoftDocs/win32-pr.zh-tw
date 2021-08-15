---
title: MDM_HealthAttestation 類別
description: MDM \_ HealthAttestation 類別可讓企業 IT 管理員評估受管理裝置的健全狀況，並採取企業原則動作。
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- MDM_HealthAttestation 類別
- MDM_HealthAttestation 類別，描述
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81d1ebf7e4df529c54dc3af125e87569ea0d300f8bb6de3a42e5b670dc43cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165811"
---
# <a name="mdm_healthattestation-class"></a>MDM \_ HealthAttestation 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ HealthAttestation** 類別可讓企業 IT 管理員評估受管理裝置的健全狀況，並採取企業原則動作。

以下是 HealthAttestation CSP 所執行的函式清單：

-   收集用來驗證裝置健康情況狀態的資料
-   將資料轉送到「健康情況證明服務」(HAS)
-   布建從中接收的健康情況證明憑證
-   在要求時，會將接收自的健康情況證明 (憑證轉寄) ，並將相關的執行時間資訊轉送至 MDM 伺服器以進行驗證

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a>成員

**MDM \_ HealthAttestation** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MDM \_ HealthAttestation** 類別具有這些方法。



| 方法                                                                 | 描述                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**VerifyHealthMethod**](mdm-healthattestation-verifyhealthmethod.md) | 通知裝置以準備健康情況憑證驗證要求的方法。<br/> |



 

### <a name="properties"></a>屬性

**MDM \_ HealthAttestation** 類別具有這些屬性。

<dl> <dt>

[[MSSQLSERVER 的通訊協定內容]](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **Octetstring**
</dt> </dl>

</dd> <dt>

[CorrelationID](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**CurrentProtocolVersion**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

TBD

</dd> <dt>

[ForceRetrieve](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[HASEndpoint](/windows/client-management/mdm/healthattestation-csp)
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

識別父節點的名稱。 此類別的字串為 "HealthAttestation"。

</dd> <dt>

**MaxSupportedProtocolVersion**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

TBD

</dd> <dt>

[Nonce](/windows/client-management/mdm/healthattestation-csp)
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

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/"

</dd> <dt>

**PreferredMaxProtocolVersion**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

TBD

</dd> <dt>

[狀態](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[TpmReadyStatus](/windows/client-management/mdm/healthattestation-csp)
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

 

