---
title: MDM_Policy_Config01_DeliveryOptimization02 類別
description: MDM \_ Policy \_ Config01 \_ DeliveryOptimization02 類別表示可用的傳遞優化原則。
ms.assetid: 10dfb751-f044-4f30-90e0-af0fcb0931fb
keywords:
- MDM_Policy_Config01_DeliveryOptimization02 類別
- MDM_Policy_Config01_DeliveryOptimization02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeliveryOptimization02
- MDM_Policy_Config01_DeliveryOptimization02.InstanceID
- MDM_Policy_Config01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb9675f87a5bf9951e125bded69ae5eb10feb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094256"
---
# <a name="mdm_policy_config01_deliveryoptimization02-class"></a>MDM \_ 原則 \_ Config01 \_ DeliveryOptimization02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ Policy \_ Config01 \_ DeliveryOptimization02** 類別表示可用的傳遞優化原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ Config01 \_ DeliveryOptimization02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ Config01 \_ DeliveryOptimization02** 類別具有這些屬性。

<dl> <dt>

[DOAbsoluteMaxCacheSize](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOAllowVPNPeerCaching](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOCacheHost](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DODownloadMode](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOGroupID](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMaxCacheAge](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMaxCacheSize](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMaxDownloadBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMaxUploadBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMinBackgroundQos](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMinBatteryPercentageAllowedToUpload](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMinDiskSizeAllowedToPeer](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMinFileSizeToCache](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMinRAMAllowedToPeer](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOModifyCacheDrive](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOMonthlyUploadDataCap](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DOPercentageMaxDownloadBandwidth](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
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

識別父節點的名稱。 此類別的字串為 ">deliveryoptimization"。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/Policy/Config"

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

