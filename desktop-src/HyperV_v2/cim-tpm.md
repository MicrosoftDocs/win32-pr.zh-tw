---
description: 描述 (TPM) 裝置的信賴平臺模組。
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: CIM_TPM 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21df36da4a84e0b85d23f24bcc839b87afa64472381aed6dbda0706374493a57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148411"
---
# <a name="cim_tpm-class"></a>CIM \_ TPM 類別

描述 (TPM) 裝置的信賴平臺模組。

## <a name="syntax"></a>語法

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a>成員

**CIM \_ TPM** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ TPM** 類別具有這些方法。



| 方法                                                         | 描述                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**ChangeOwnerAuth**](cim-tpm-changeownerauth.md)             | 變更 TPM 裝置的擁有者授權認證。<br/>                                                  |
| [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) | 要求將 TPM 的狀態變更為 **RequestedTPMState** 參數中指定的值。<br/> |



 

### <a name="properties"></a>屬性

**CIM \_ TPM** 類別具有這些屬性。

<dl> <dt>

**AvailableRequestedTPMStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ TPM**」。**RequestTPMStateChange**，CIM \_ TPMCapabilities. RequestedTPMStatesSupported ") 
</dt> </dl>

[**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md)方法之 *RequestedTPMState* 參數的可能值。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**已啟用 S1-Active-擁有的** (2) 


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 已停用-Active-擁有的** (3) 


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**已啟用 S3-非使用中-擁有的** (4) 


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**已停用 S4-非使用中-擁有的** (5) 


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**已啟用 S5-主動-** 無人擁有的 (6) 


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 已停用-主動-** 無人 (7) 


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 已啟用-非** 使用中-無人擁有的 (8) 


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 已停用-非** 使用中-無人擁有的 (9) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TPMManafucturerMajorRevision**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 2 v1dot2 \| Section 5.3 \| version \| revMajor ") 
</dt> </dl>

TPM 的製造商主要修訂。

</dd> <dt>

**TPMManufacturerId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| 第2部分 v1dot2 \| 區段 \| 21.6 \_ TPM CAP \_ 版本 \_ 資訊 \| tpmVendorID ") 
</dt> </dl>

TPM 製造商識別碼。

</dd> <dt>

**TPMManufacturerInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 2 v 1.2. a \| r 區段 21.6 \| TPM \_ CAP \_ VERSION \_ INFO \| vendorSpecific ") 
</dt> </dl>

TPM 製造商所定義的其他資訊。

</dd> <dt>

**TPMManufacturerMinorRevision**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 2 v1dot2 \| Section 5.3 \| version \| revMinor ") 
</dt> </dl>

TPM 的製造商次要修訂。

</dd> <dt>

**TPMSpecMajorVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| 第2部分 v1dot2 \| 第 5.3 \| 版 \| 的主要 "，" TSS。TCG \| Level 1 V1.1 \| 區段 2.3.2.18 ") 
</dt> </dl>

TPM 的主要版本。

</dd> <dt>

**TPMSpecMinorVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| 第2部分 v1dot2 \| 第 5.3 \| 版 \| 次要版 "，" TSS。TCG \| Level 1 V1.1 \| 區段 2.3.2.18 ") 
</dt> </dl>

TPM 的次要版本。

</dd> <dt>

**TPMState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 TPM。TCG \| Part 1 v1dot2 \| Section 9.4 "，" TPM。TCG \| 第2部分 v1dot2 \| 區段 7.1 \| tpm \_ 永久 \_ 旗標 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ tpm**。**RequestTPMStateChange**"，"**CIM \_ TPM**.**TransitioningToTPMState**") 
</dt> </dl>

TPM 的操作狀態。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**已啟用 S1-Active-擁有的** (2) 


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 已停用-Active-擁有的** (3) 


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**已啟用 S3-非使用中-擁有的** (4) 


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**已停用 S4-非使用中-擁有的** (5) 


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**已啟用 S5-主動-** 無人擁有的 (6) 


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 已停用-主動-** 無人 (7) 


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 已啟用-非** 使用中-無人擁有的 (8) 


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 已停用-非** 使用中-無人擁有的 (9) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (10) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TransitioningToTPMState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ TPM**」。**RequestTPMStateChange**"，"**CIM \_ TPM**.**TPMState**") 
</dt> </dl>

TPM 正在轉換的目標狀態。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**已啟用 S1-Active-擁有的** (2) 


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 已停用-Active-擁有的** (3) 


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**已啟用 S3-非使用中-擁有的** (4) 


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**已停用 S4-非使用中-擁有的** (5) 


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**已啟用 S5-主動-** 無人擁有的 (6) 


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 已停用-主動-** 無人 (7) 


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 已啟用-非** 使用中-無人擁有的 (8) 


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 已停用-非** 使用中-無人擁有的 (9) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (10) 


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**沒有變更** (11) 


</dt> <dd></dd> <dt>



  (12) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

