---
description: Win32 \_ PnPDevice 關聯 WMI 類別會將已知的裝置 (設定管理員為 PNPEntity) 以及它所執行的函式。
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a136c86c0fd0744c555af2071943d99ca8569a33ce9c59d9d22191c4a78d2a32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972038"
---
# <a name="win32_pnpdevice-class"></a>Win32 \_ PnPDevice 類別

**Win32 \_ PnPDevice** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將已知的裝置 (設定管理員為 PNPEntity) 以及它所執行的函式。 它的函式是以描述其使用方式的邏輯裝置子類別表示。 例如， [**win32 \_ 鍵盤**](win32-keyboard.md) 或 [**win32 \_ DiskDrive**](win32-diskdrive.md) 實例。 這兩個參考的物件都代表相同的基礎系統裝置;PNPEntity 端資源配置的變更將會影響相關聯的裝置。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>成員

**Win32 \_ PnPDevice** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PnPDevice** 類別具有這些屬性。

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "cim \| cim \_ LogicalDevice" ) 
</dt> </dl>

參考 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 實例，表示與隨插即用裝置相關聯的邏輯裝置屬性。

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ PnPEntity**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PnPEntity" ) 
</dt> </dl>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)實例的參考，代表與邏輯裝置相關聯的隨插即用裝置。

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

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
