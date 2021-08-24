---
description: CIM \_ HostedBootService 類別會將主機系統和開機服務產生關聯。 由於此關聯性是從 CIM HostedService 子類別化 \_ ，因此它會繼承為服務定義的範圍/命名配置，其中服務會延遲至其主機系統。
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: CIM_HostedBootService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: abfd506a3962e05a8ab1087dc3a5dc43d4cd74fac08fac7344d3ff22fff49909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921678"
---
# <a name="cim_hostedbootservice-class"></a>CIM \_ HostedBootService 類別

**CIM \_ HostedBootService** 類別會將主機系統和開機服務產生關聯。 由於此關聯性是從 [**CIM \_ HostedService**](cim-hostedservice.md)子類別化，因此它會繼承為服務定義的範圍/命名配置，其中服務會延遲至其主機系統。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a>成員

**CIM \_ HostedBootService** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ HostedBootService** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 系統**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (前) 
</dt> </dl>

描述裝載系統的 [**CIM \_ 系統**](cim-system.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ BootService**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ BootService**](cim-bootservice.md) ，描述系統上裝載的開機服務。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ HostedBootService** 類別衍生自 [**cim \_ HostedService**](cim-hostedservice.md)。

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> </dl>

 

