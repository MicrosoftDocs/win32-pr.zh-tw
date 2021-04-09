---
description: CIM \_ CollectionOfMSEs 物件允許將 cim \_ ManagedSystemElement 物件分組，以建立設定和設定的關聯性。 它是抽象的，需要在子類別中進行進一步的定義和語義改進。
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: 'CIM_CollectionOfMSEs 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110993"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs 類別 (CIMWin32 WMI 提供者) 

**Cim \_ CollectionOfMSEs** 物件允許將 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)物件分組，以建立設定和設定的關聯性。 它是抽象的，需要在子類別中進行進一步的定義和語義改進。

**CIM \_ CollectionOfMSEs** 物件不會包含任何狀態或狀態資訊，但只代表元素群組。 基於這個理由，從 **cim \_ CollectionOfMSEs** 具有狀態/狀態的子類別化群組不正確，例如 [**Cim \_ RedundancyGroup**](cim-redundancygroup.md) (從 [**cim \_ LogicalElement**](cim-logicalelement.md)) 正確子類別。 集合通常會匯總「贊」物件，並表示優化。 如果沒有集合，則會強制定義個別的 [**cim \_ ElementSetting**](cim-elementsetting.md) 和 [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) 關聯，以將設定和設定物件系結至個別的 [**cim \_ ManagedSystemElements**](cim-managedsystemelement.md)。 將相同的設定指派給多個物件時，可能會有很多重複。 此外，使用 collection 物件可判斷集合成員的設定和設定關聯確實相同。 這項資訊的取得方式是以專屬的方式定義集合，然後查詢 **CIM \_ ElementSetting** 和 **cim \_ ElementConfiguration** 關聯，以判斷是否已完全涵蓋該收集組。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a>成員

**CIM \_ CollectionOfMSEs** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ CollectionOfMSEs** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

CollectionOfMSEs 物件的簡短文字描述。

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

集合物件的識別。 子類別化時，CollectionID 屬性可以覆寫為索引鍵屬性。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

CollectionOfMSEs 物件的文字描述。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。 請參閱衍生自 **CIM \_ COLLECTIONOFMSES** 之 WMI 類別的 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




