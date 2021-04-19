---
description: 將 Msvm \_ SnapshotCollection 與包含的 Msvm \_ VirtualSystemSettingData 物件產生關聯。
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Msvm_CollectedSnapshots 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979033"
---
# <a name="msvm_collectedsnapshots-class"></a>Msvm \_ CollectedSnapshots 類別

將 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 與包含的 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 物件產生關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a>成員

**Msvm \_ CollectedSnapshots** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ CollectedSnapshots** 類別具有這些屬性。

<dl> <dt>

**集合**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ SnapshotCollection**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Collection" ) 
</dt> </dl>

代表集合的 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 群組或 ' 包 ' 物件。

</dd> <dt>

**成員**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ VirtualSystemSettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Member" ) 
</dt> </dl>

包含集合成員的 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> </dl>

 

