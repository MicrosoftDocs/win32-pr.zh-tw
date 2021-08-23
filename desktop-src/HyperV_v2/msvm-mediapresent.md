---
description: 將存放磁片磁碟機與插入磁片磁碟機的媒體產生關聯。
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Msvm_MediaPresent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7044cfed5a4affd628ea8008c89b4aabeee3499d65f03abf815e68d73d06a773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521718"
---
# <a name="msvm_mediapresent-class"></a>Msvm \_ MediaPresent 類別

將存放磁片磁碟機與插入磁片磁碟機的媒體產生關聯。 此關聯用於所有存放磁片磁碟機物件。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>成員

**Msvm \_ MediaPresent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ MediaPresent** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

媒體存取裝置的參考。 這個屬性繼承自 [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用媒體存取裝置存取的儲存範圍參考。 這個屬性繼承自 [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)。

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出存取的儲存區是否為固定的，且無法被退出。 硬碟的值為 **True** ，否則為 **False** 。 這個屬性繼承自 [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ MediaPresent** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dt>

[**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[儲存體類](storage-classes.md)
</dt> </dl>

 

