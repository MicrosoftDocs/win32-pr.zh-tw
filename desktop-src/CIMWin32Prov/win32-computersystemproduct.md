---
description: 代表產品。 這包括此電腦系統上所使用的軟體和硬體。
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Win32_ComputerSystemProduct 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47312acde8f346ac4ac3b2260fe06a2a5270610f9b7265da2b627a4c92fb4b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119294028"
---
# <a name="win32_computersystemproduct-class"></a>Win32 \_ ComputerSystemProduct 類別

**Win32 \_ ComputerSystemProduct** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表產品。 這包括此電腦系統上所使用的軟體和硬體。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a>成員

**Win32 \_ ComputerSystemProduct** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ComputerSystemProduct** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

產品的簡短文字描述。

這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

產品的文字描述。

這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.4 ") 
</dt> </dl>

產品識別，例如軟體序號、硬體晶片上的骰子號碼，或) 專案編號的非商業性產品 (。

這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.2 ") 
</dt> </dl>

常用的產品名稱。

這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。

</dd> <dt>

**SKUNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

產品的庫存單位 (SKU) 資訊。

這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。

</dd> <dt>

**UUID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 1 \| UUID" ) 
</dt> </dl>

此產品 (UUID) 的通用唯一識別碼。 UUID 是128位的識別碼，保證與其他產生的 Uuid 不同。 如果 UUID 無法使用，則會使用所有零的 UUID。

此值來自 SMBIOS 資訊中 **系統資訊** 結構的 **UUID** 成員。

</dd> <dt>

**廠商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 元件 \| 001.1 ") 
</dt> </dl>

產品供應商的名稱，或銷售產品的實體 (製造商、轉售商、OEM 等) 。

這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.3 ") 
</dt> </dl>

產品版本資訊。

這個屬性繼承自 [**CIM \_ 產品**](cim-product.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ ComputerSystemProduct** 類別衍生自 [**CIM \_ 產品**](cim-product.md)。

## <a name="examples"></a>範例

TechNet 資源庫上的 [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell 範例會使用 **Win32 \_ COMPUTERSYSTEMPRODUCT** ，以使用 WMI 抓取無法運作的硬體清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 產品**](cim-product.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

