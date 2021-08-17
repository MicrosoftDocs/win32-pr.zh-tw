---
description: 虛擬系統與快照集（虛擬系統的父系）間的設定資料之間的關聯。
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: CIM_PreviousSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 85f08f22409df8a17bdae33ae81c06cb8167996ecb477f6a2d207d9e0ce2acca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131760"
---
# <a name="cim_previoussettingdata-class"></a>CIM \_ PreviousSettingData 類別

虛擬系統與快照集（虛擬系統的父系）間的設定資料之間的關聯。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a>成員

**CIM \_ PreviousSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ PreviousSettingData** 類別具有這些屬性。

<dl> <dt>

**PreviousObject**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

此電腦系統父系的快照集設定資料。

</dd> <dt>

**Target**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

應用程式目標的電腦系統。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------|
| 命名空間<br/> | 根 \\ CIMV2<br/> |



 

 




