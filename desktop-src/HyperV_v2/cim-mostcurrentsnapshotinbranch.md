---
description: 表示虛擬系統與系統最新快照之間的關聯。 只有在使用快照集建立虛擬系統，或是從虛擬系統建立快照集時，此關聯才會存在。
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: CIM_MostCurrentSnapshotInBranch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: de94bf0e6f88240ac89eb62de881540f5c747b7a1d0ec13307e7e5d35fe53da4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694968"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a>CIM \_ MostCurrentSnapshotInBranch 類別

表示虛擬系統與系統最新快照之間的關聯。 只有在使用快照集建立虛擬系統，或是從虛擬系統建立快照集時，此關聯才會存在。

## <a name="syntax"></a>語法

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>成員

**CIM \_ MostCurrentSnapshotInBranch** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ MostCurrentSnapshotInBranch** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

代表虛擬系統之 CIM 系統 [**實例 \_**](cim-computersystem.md) 的參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ VirtualSystemSettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

表示虛擬系統快照集之 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 實例的參考。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

