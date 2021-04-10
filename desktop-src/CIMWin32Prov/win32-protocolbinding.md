---
description: Win32 \_ ProtocolBinding 關聯 WMI 類別會將系統層級的驅動程式、網路通訊協定和網路介面卡相關聯。
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Win32_ProtocolBinding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847078"
---
# <a name="win32_protocolbinding-class"></a>Win32 \_ ProtocolBinding 類別

**Win32 \_ ProtocolBinding** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將系統層級的驅動程式、網路通訊協定和網路介面卡相關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a>成員

**Win32 \_ ProtocolBinding** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ProtocolBinding** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ NetworkProtocol**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ NetworkProtocol" ) 
</dt> </dl>

此實例的參考，代表與系統驅動程式和網路介面卡搭配使用的通訊協定。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ >systemdriver**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ >systemdriver" ) 
</dt> </dl>

此實例的參考，代表透過此類別的網路通訊協定使用網路介面卡的系統驅動程式。

</dd> <dt>

**裝置**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ NetworkAdapter**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ NetworkAdapter" ) 
</dt> </dl>

電腦系統上所使用網路介面卡的屬性。

</dd> </dl>

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

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
