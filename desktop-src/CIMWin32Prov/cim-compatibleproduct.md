---
description: CIM \_ CompatibleProduct 類別代表產品之間的關聯，表示兩個參考的產品是否可互通，例如是否可以一起安裝，或是可以是另一個實體容器，依此類推。
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: CIM_CompatibleProduct 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d0d4721d8554723bb9ab808ff55884bb896f59e6050103cf127cc4df77109f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080872"
---
# <a name="cim_compatibleproduct-class"></a>CIM \_ CompatibleProduct 類別

**CIM \_ CompatibleProduct** 類別代表產品之間的關聯，表示兩個參考的產品是否可互通，例如是否可以一起安裝，或是可以是另一個實體容器，依此類推。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a>成員

**CIM \_ CompatibleProduct** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ CompatibleProduct** 類別具有這些屬性。

<dl> <dt>

**CompatibilityDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式的字串，可定義兩個參考的產品如何互通、相容，以及是否有相容性限制。

</dd> <dt>

**CompatibleProduct**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 產品**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

相容產品的參考。

</dd> <dt>

**產品**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 產品**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考已定義相容產品的產品。

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



 

 




