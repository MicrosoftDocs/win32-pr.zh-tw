---
description: CIM \_ FRUPhysicalElements 類別代表組成現場可更換單元 (FRU) 的實體元素。
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: CIM_FRUPhysicalElements 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936312"
---
# <a name="cim_fruphysicalelements-class"></a>CIM \_ FRUPhysicalElements 類別

**CIM \_ FRUPhysicalElements** 類別代表組成現場可更換單元 (FRU) 的實體元素。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a>成員

**CIM \_ FRUPhysicalElements** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ FRUPhysicalElements** 類別具有這些屬性。

<dl> <dt>

**元件**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考屬於 FRU 一部分的實體元素。

</dd> <dt>

**FRU**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ FRU**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

FRU 的參考。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

