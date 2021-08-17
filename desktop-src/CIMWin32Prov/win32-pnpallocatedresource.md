---
description: Win32 \_ PnPAllocatedResource 關聯 WMI 類別代表邏輯裝置與系統資源之間的關聯。
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Win32_PnPAllocatedResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 492bd510965499393b399e8e02c1b901fc33f9abc00acf191899c5bb6b8b6d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118008942"
---
# <a name="win32_pnpallocatedresource-class"></a>Win32 \_ PnPAllocatedResource 類別

**Win32 \_ PnPAllocatedResource** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)代表邏輯裝置與系統資源之間的關聯。 此類別是用來探索特定裝置使用中的資源，例如插斷要求 (IRQ) 或直接記憶體存取 (DMA) 通道。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ PnPAllocatedResource** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PnPAllocatedResource** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SystemResource**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ SystemResource" ) 
</dt> </dl>

[**CIM \_ SystemResource**](cim-systemresource.md)實例的參考，代表可供邏輯裝置使用之系統資源的屬性。 這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ PnPEntity**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「cim \| CIM \_ LogicalDevice」 ) 
</dt> </dl>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)實例的參考，該實例會使用指派給它的系統資源來表示邏輯裝置的屬性。 這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PnPAllocatedResource** 類別衍生自 [**CIM \_ AllocatedResource**](cim-allocatedresource.md)。

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

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
