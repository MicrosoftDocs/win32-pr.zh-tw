---
description: 定義參考的獨立系統所符合的已註冊設定檔。
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Msvm_StandaloneV2ElementConformsToProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943772"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>Msvm \_ StandaloneV2ElementConformsToProfile 類別

定義參考的獨立系統所符合的已註冊設定檔。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>成員

**Msvm \_ StandaloneV2ElementConformsToProfile** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ StandaloneV2ElementConformsToProfile** 類別具有這些屬性。

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ RegisteredProfile**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

獨立系統符合的已註冊設定檔。

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)、 **MSFT \_ TargetNamespace** ( 「根 \\ \\ 虛擬化 \\ \\ v2」 ) 
</dt> </dl>

符合已註冊設定檔的獨立系統。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ ElementConformsToProfile**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

