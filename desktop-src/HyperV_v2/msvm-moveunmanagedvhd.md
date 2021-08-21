---
description: 將虛擬硬碟從來源移到目的地路徑。
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Msvm_MoveUnmanagedVhd 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e631b95c9961262df288b76cf83f953589780c2feb294e940314d08975bcfd57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521118"
---
# <a name="msvm_moveunmanagedvhd-class"></a>Msvm \_ MoveUnmanagedVhd 類別

將虛擬硬碟從來源移到目的地路徑。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a>成員

**Msvm \_ MoveUnmanagedVhd** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ MoveUnmanagedVhd** 類別具有這些屬性。

<dl> <dt>

**VhdDestinationPath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目的地路徑。

</dd> <dt>

**VhdSourcePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要移動之虛擬硬碟的來源路徑。

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

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

 




