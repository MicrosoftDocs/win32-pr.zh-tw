---
description: CIM \_ ManagedElement 類別是一種抽象類別，可針對 CIM 架構中的非關聯類別，提供通用超類別 (或繼承樹狀結構的最上層) 。
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973602"
---
# <a name="cim_managedelement-class"></a>CIM \_ ManagedElement 類別

**Cim \_ ManagedElement** 類別是一種抽象類別，可針對 CIM 架構中的非關聯類別，提供通用超類別 (或繼承樹狀結構的最上層) 。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a>成員

**CIM \_ ManagedElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ManagedElement** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

物件的簡短文字描述。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的文字描述。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的易記名稱。 這個屬性可讓每個實例定義使用者易記名稱，以及其索引鍵屬性、身分識別資料和描述資訊。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在包含的命名空間範圍內，以獨特且不透明的方式識別此類別的實例。

> [!IMPORTANT]
>
> 為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*
>
> *OrgID* 必須包含受著作權、商標或其他唯一名稱（由定義 **InstanceID** 的商務實體所擁有），或是由可辨識的全域授權單位所指派的註冊識別碼。 此模式類似于架構類別名稱的結構。 此外，若要確保唯一性， **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。 因此， *OrgID* 不能包含冒號 ( '： ' ) 。
>
> *LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。
>
> 如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。
>
> 若為分散式管理工作強制 (DMTF) 定義的實例，則必須搭配 *OrgID* 設定為 CIM 使用模式。

 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

