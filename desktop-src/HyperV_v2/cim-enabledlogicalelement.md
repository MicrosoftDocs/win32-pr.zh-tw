---
description: 表示可以啟用和停用的邏輯元素。
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: CIM_EnabledLogicalElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974300"
---
# <a name="cim_enabledlogicalelement-class"></a>CIM \_ EnabledLogicalElement 類別

表示可以啟用和停用的邏輯元素。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a>成員

**CIM \_ EnabledLogicalElement** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ EnabledLogicalElement** 類別具有這些方法。



| 方法                                                                     | 描述                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) | 要求將元素的狀態變更為指定的值。<br/> |



 

### <a name="properties"></a>屬性

**CIM \_ EnabledLogicalElement** 類別具有這些屬性。

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**RequestStateChange**"，"[**CIM \_ EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md)。**RequestedStatesSupported**") 
</dt> </dl>

指出 [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md)方法的 *RequestedState* 參數可能的值。

列出的值必須是相關聯之 **CIM \_ EnabledLogicalElementCapabilities** 實例之 **RequestedStatesSupported** 屬性中所包含之值的子集。 如果實值無法判斷元素目前狀態的可能值，則這個屬性為 **Null** 。

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**關機** (4) 


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**離線** (6) 


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**測試** (7) 


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**延** 後 (8) 


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**靜止** (9) 


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**重新開機** (10) 


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**重設** (11) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出專案的已啟用狀態之系統管理員的預設或啟動設定。 預設值 **已啟用** (2) 。

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (5) 


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

**已啟用但離線** (6) 


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

**沒有預設** (7) 


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**靜止** (9) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**OtherEnabledState**") 
</dt> </dl>

指出專案的已啟用狀態。 可能的值包括狀態之間的轉換。 例如， **關閉** (4) 並 **啟動** (10) 是 **啟用** 和 **停用** 之間的暫時性狀態。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 


</dt> <dd>

元素是或可能正在執行命令、將會處理任何已排入佇列的命令，並將新的要求排入佇列。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 


</dt> <dd>

元素將不會執行命令，而且會卸載任何新的要求。

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (4) 


</dt> <dd>

專案正在進入已停用狀態的進程。

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (5) 


</dt> <dd>

元素不支援啟用或停用。

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) 


</dt> <dd>

元素可能正在完成命令，並會卸載任何新的要求。

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (7) 


</dt> <dd>

元素處於測試狀態。

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**延** 後的 (8) 


</dt> <dd>

元素可能正在完成命令，但是會將任何新的要求排在佇列中。

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) 


</dt> <dd>

元素已啟用但處於受限模式。

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (10) 


</dt> <dd>

元素正在進入已啟用的狀態。 新的要求會排入佇列。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (11. 32767) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**EnabledState**") 
</dt> </dl>

描述當 **EnabledState** 屬性的值是 **其他** 時，元素的狀態。 當 **EnabledState** 不是 **其他** 值時，這個屬性必須設定為 **Null** 。

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**EnabledState**") 
</dt> </dl>

表示最後要求的元素狀態。 目前的狀態是由 **EnabledState** 屬性工作表示。 這個屬性可讓您比較最後要求和目前的狀態。

> [!Note]  
> 當 **EnabledState** 屬性的值 **不適用** 時，這個屬性不會有任何意義。

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

最後要求的元素狀態不明。

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 


</dt> <dd>

要求立即停用元素，使其不會執行或接受任何命令或處理要求。

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) 


</dt> <dd>

要求有條理地轉換為停用狀態，而且可能需要移除電源，以完全清除任何現有的狀態。

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**沒有變更** (5) 


</dt> <dd>

已淘汰，用來表示最後要求的狀態為「未知」 (0) 。 如果上次要求或預期的狀態不明，則 **RequestedState** 的值應為「未知」 (0) ，但可能會有「沒有變更」值 (5) 。

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) 


</dt> <dd>

已要求將元素轉換成已啟用但離線的 **EnabledState**。

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) 


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**延** 後的 (8) 


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) 


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) 


</dt> <dd>

指的是「關機」，然後移至「已啟用」狀態。

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) 


</dt> <dd>

指出元素是先「停用」，然後是「已啟用」。

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (12) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出元素上次變更狀態的時間。 如果專案的狀態未變更，而且此屬性已填入，則必須將它設定為零間隔值。 如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElement**.**RequestStateChange**"，"**CIM \_ EnabledLogicalElement**。**RequestedState**"，"**CIM \_ EnabledLogicalElement**。**EnabledState**") 
</dt> </dl>

指出實例要變更的目標狀態。

**沒有變更** 的值表示沒有正在進行的轉換。 [ **不適用** ] 的值表示執行不會報告進行中的轉換。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**關機** (4) 


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

**沒有變更** (5) 


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**離線** (6) 


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**測試** (7) 


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**延** 後 (8) 


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**靜止** (9) 


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**重新開機** (10) 


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**重設** (11) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (12) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

