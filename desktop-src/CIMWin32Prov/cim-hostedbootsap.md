---
description: CIM \_ HostedBootSAP 類別會定義 cim BootSAP 類別的裝載單一電腦系統 \_ 。
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: CIM_HostedBootSAP 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936310"
---
# <a name="cim_hostedbootsap-class"></a>CIM \_ HostedBootSAP 類別

**Cim \_ HostedBootSAP** 類別會定義 [**cim \_ BootSAP**](cim-bootsap.md)類別的裝載單一電腦系統。 由於此關聯性是從 [**cim \_ HostedAccessPoint**](cim-hostedaccesspoint.md)子類別化，因此它會繼承針對 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)定義的範圍/命名配置，其中存取點會延遲至其主機系統。 在此情況下， **CIM \_ BootSAP** 必須延後至其裝載的 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) 類別。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ HostedBootSAP** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ HostedBootSAP** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ UnitaryComputerSystem**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述單一電腦系統的 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ BootSAP**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ BootSAP**](cim-bootsap.md) ，描述裝載于單一電腦系統上的開機 SAP。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ HostedBootSAP** 類別衍生自 [**cim \_ HostedAccessPoint**](cim-hostedaccesspoint.md)。

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

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)
</dt> </dl>

 

