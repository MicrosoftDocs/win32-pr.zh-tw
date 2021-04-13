---
title: 'SoHAttributeValue 聯集 (NapProtocol .h) '
description: 在 SoHAttribute 結構中定義型別成員的內容。
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- SoHAttributeValue 聯集 NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466457"
---
# <a name="sohattributevalue-union"></a>SoHAttributeValue 聯集

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**SoHAttributeValue** 聯集會在 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)結構中定義 **型** 別成員的內容。 **SoHAttributeValue** 聯集的結構取決於 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)結構的 **型** 別成員中指定的 [**SoHAttributeType**](sohattributetype-enum.md) 。

## <a name="syntax"></a>語法


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a>成員

<dl> <dt>

**idVal**
</dt> <dd>

**案例 (sohAttributeTypeSystemHealthId)**

包含系統健康狀態代理程式識別碼的唯一 [SystemHealthEntityId](nap-datatypes.md) ， (SHA) 或系統健康狀態驗證， (建立此 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包的 SHV) 。

</dd> <dt>

**v4AddressesVal**
</dt> <dd>

**案例 (sohAttributeTypeIpv4FixupServers)**

NAP 系統正在使用的修正伺服器的 IPv4 位址。

<dl> <dt>

**計數**
</dt> <dd>

介於1到 [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md)的 **位址** 成員中的 IPv4 位址數目。

</dd> <dt>

**位址**
</dt> <dd>

[**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address)結構的陣列，其中包含 IPv4 位址。

</dd> </dl> </dd> <dt>

**v6AddressesVal**
</dt> <dd>

**案例 (sohAttributeTypeIpv6FixupServers)**

NAP 系統正在使用的修正伺服器 IPv6 位址。

<dl> <dt>

**計數**
</dt> <dd>

介於1到 [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md)的 **位址** 成員中的 IPv4 位址數目。

</dd> <dt>

**位址**
</dt> <dd>

[**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address)結構的陣列，其中包含 IPv4 位址。

</dd> </dl> </dd> <dt>

**codesVal**
</dt> <dd>

**案例 (sohAttributeTypeComplianceResultCodes、sohAttributeTypeErrorCodes)**

[**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes)結構，其中包含應用程式定義的用戶端或 [**NAP 錯誤常數**](nap-error-constants.md)的合規性結果碼。 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包必須包含此 Tlv 或 **sohAttributeTypeFailureCategory** 的 tlv。

</dd> <dt>

**dateTimeVal**
</dt> <dd>

**案例 (sohAttributeTypeTimeOfLastUpdate、sohAttributeTypeSoHGenerationTime)**

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構，其中包含上次 [**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)更新或 **SoH** 產生時間的時間。

</dd> <dt>

**vendorSpecificVal**
</dt> <dd>

**案例 (sohAttributeTypeVendorSpecific)**

由廠商定義的應用程式特定資料。

<dl> <dt>

**vendorId**
</dt> <dd>

4位元組的識別碼，定義 SHA/SHV 配對識別碼。 前3個位元組是供應商的 IETF 指派 SMI-S 碼，最後一個位元組會識別元件本身。 在執行 SHA 或 SHV 時，請勿使用指派給 [**NAP 廠商常數**](nap-vendor-constants.md)上內部 Microsoft 系統健康情況元件的識別碼值。

</dd> <dt>

**size**
</dt> <dd>

從0到 ([**maxSoHAttributeSize**](nap-type-constants.md) -4) 範圍中廠商資料的大小（以位元組為單位）。

</dd> <dt>

**vendorSpecificData**
</dt> <dd>

以網路位元組順序排列之廠商特定資料的指標。

</dd> </dl> </dd> <dt>

**uint8Val**
</dt> <dd>

**案例 (sohAttributeTypeHealthClass、sohAttributeTypeFailureCategory、sohAttributeTypeExtendedIsolationState)**

NAP 元件的健全狀況類別、失敗類別或擴充隔離狀態，表示為 [**HealthClassValue**](healthclassvalue-enum.md) 或 [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) 值，或 [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) 結構。

</dd> <dt>

**octetStringVal**
</dt> <dd>

**預設值**

下列屬性的值是八位字串：

-   sohAttributeTypeSoftwareVersion
-   sohAttributeTypeClientId
-   sohAttributeTypeProductName
-   sohAttributeTypeHealthClassStatus

基於向前相容性，所有無法辨識的屬性都會以八位字串的形式傳回。 **資料** 必須以網路位元組順序排序。

<dl> <dt>

**size**
</dt> <dd>

範圍0到 [**maxSoHAttributeSize**](nap-type-constants.md)的 **資料** 大小（以位元組為單位）。

</dd> <dt>

**data**
</dt> <dd>

八位字串值的指標。

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a>實際資料版面配置

由於 SDK 發行環境的本質，在語法區塊中不會清楚地表示等位。 以下是 NapProtocol .h 標頭檔中的實際語法。


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a>備註

NAP 系統會使用這些屬性類型：

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

[**SoHAttributeTypes**](sohattributetype-enum.md)的其餘部分純粹是 Sha 和 shv 使用的規範性指導方針。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 參考](nap-reference.md)
</dt> <dt>

[NAP 結構](nap-structures.md)
</dt> </dl>

 

