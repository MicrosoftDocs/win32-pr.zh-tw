---
description: 表示其他集合的集合。
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Msvm_ManagementCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979391"
---
# <a name="msvm_managementcollection-class"></a>Msvm \_ ManagementCollection 類別

表示其他集合的集合。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a>成員

**Msvm \_ ManagementCollection** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ManagementCollection** 類別具有這些屬性。

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CollectionID" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

集合物件的唯一識別碼。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ElementName" ) 
</dt> </dl>

集合的使用者定義名稱。 請注意，這不一定是唯一的。

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

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> </dl>

 

