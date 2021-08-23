---
description: 定義所參考系統符合的已註冊設定檔。
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a80dfcb5ab260b4d60b6370bb34698efb201401f0c6d4924b143e8b9041258a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525048"
---
# <a name="msvm_elementconformstoprofile-class"></a>Msvm \_ ElementConformsToProfile 類別

定義所參考系統符合的已註冊設定檔。 這個關聯可能會套用至任何 managed 元素。 一般使用方式會將它套用至較高層級的實例，例如系統、命名空間或服務。 當套用至較高層級的實例時，所有組成零件都必須適當地運作，以支援受管理元素與已命名之註冊設定檔的一致性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>成員

**Msvm \_ ElementConformsToProfile** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ElementConformsToProfile** 類別具有這些屬性。

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)類別實例的參考，表示系統符合的已註冊設定檔。

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_**](msvm-computersystem.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表符合已註冊設定檔的系統。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

