---
description: CIM \_ FRU 類別代表廠商定義的產品和實體元素集合，與現場可更換單元相關聯 (FRU) 在客戶的位置支援、維護或升級產品。
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: CIM_FRU 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b87d1cb3719da794f2f9cb89f4698c3452769c7213d6fc7d58885585c18c4a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923698"
---
# <a name="cim_fru-class"></a>CIM \_ FRU 類別

**CIM \_ FRU** 類別代表廠商定義的產品和實體元素集合，與現場可更換單元相關聯 (FRU) 在客戶的位置支援、維護或升級產品。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a>成員

**CIM \_ FRU** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ FRU** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

FRU 的簡短文字描述。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.3」 ) 
</dt> </dl>

FRU 的描述。

</dd> <dt>

**FRUNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.6 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

FRU 訂購資訊。

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.7 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

識別軟體，例如序號或硬體晶片上的骰子編號。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

已知物件的標籤。

</dd> <dt>

**RevisionLevel**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.8 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

FRU 的修訂層級。

</dd> <dt>

**廠商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.4 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

供應商的名稱。

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



 

