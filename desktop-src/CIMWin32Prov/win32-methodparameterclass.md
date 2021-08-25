---
description: Win32 \_ MethodParameterClass abstract、BASE WMI 類別會衍生任何定義為參數值容器的類別，這些值會傳遞給方法。
ms.assetid: 293fa378-432d-4e97-a8ab-8dc4917d5476
ms.tgt_platform: multiple
title: Win32_MethodParameterClass 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MethodParameterClass
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a6477235b6046fad2767cad35fe7aaad3fa4ae7003106b619e9d8b33150d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973021"
---
# <a name="win32_methodparameterclass-class"></a>Win32 \_ MethodParameterClass 類別

**Win32 \_ MethodParameterClass** Abstract、base [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會衍生任何定義為參數值容器的類別，這些值會傳遞給方法。 沒有本身的屬性，這個類別會做為分類節點。 [**CIM \_ PhysicalElement**](cim-physicalelement.md)就是一個類似的範例。 從 **CIM \_ PhysicalElement** 衍生表示類別會描述實體，而不是邏輯實體。 在 **Win32 \_ MethodParameterClass** 的情況下，會特別建立從中衍生的類別，以便將參數傳遞給方法。

## <a name="syntax"></a>語法

## <a name="members"></a>成員

**Win32 \_ MethodParameterClass** 類別不會定義任何成員。

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

[WMI 服務管理類別](/windows/desktop/CIMWin32Prov/wmi-service-management-classes)
</dt> </dl>

 

