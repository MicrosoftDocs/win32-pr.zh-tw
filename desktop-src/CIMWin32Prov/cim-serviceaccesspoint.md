---
description: CIM \_ ServiceAccessPoint 類別代表使用或叫用服務的能力。 存取點代表可供其他實體使用的服務。
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: 'CIM_ServiceAccessPoint 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7dbabaa1ddaba8e557d745318a775f906aae7036379bfcf39f42d09d569e650f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919638"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a>CIM_ServiceAccessPoint 類別 (CIMWin32 WMI 提供者) 

**CIM \_ ServiceAccessPoint** 類別代表使用或叫用服務的能力。 存取點代表可供其他實體使用的服務。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a>成員

**CIM \_ ServiceAccessPoint** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ServiceAccessPoint** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

可唯一識別服務存取點，並提供所管理功能的指示。 此功能在物件的 Description 屬性中有更詳細的說明。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

表示物件目前狀態的字串。 您可以定義操作和非運作狀態。 操作狀態可以包含「確定」、「降級」和「Pred 失敗」。 「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。

非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。 「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

範圍系統的建立類別名稱。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

範圍系統的名稱。

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 
</dt> </dl>

SAP 的類型，例如 [已連接] 或 [已重新導向]。

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**寫入** (1) 


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**閱讀** (2) 


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

重新 **導向** (4) 


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

**Net \_附加** (8) 


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (16) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ ServiceAccessPoint** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。

WMI 不會執行這個類別。 針對衍生自 **CIM \_ SERVICEACCESSPOINT** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。

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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

