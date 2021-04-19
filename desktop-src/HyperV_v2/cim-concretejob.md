---
description: CIM 作業類別的具體版本 \_ 。 此類別代表要執行的一般可具現化工作單位，例如批次或列印工作。
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970238"
---
# <a name="cim_concretejob-class"></a>CIM \_ ConcreteJob 類別

[**CIM \_ 作業**](cim-job.md)類別的具體版本。 此類別代表要執行的一般可具現化工作單位，例如批次或列印工作。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a>成員

**CIM \_ ConcreteJob** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ ConcreteJob** 類別具有這些方法。



| 方法                                                           | 描述                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | 抓取實體作業之操作狀態的錯誤資訊。<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | 要求實體作業的指定狀態變更。<br/>                    |



 

### <a name="properties"></a>屬性

**CIM \_ ConcreteJob** 類別具有這些屬性。

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) 
</dt> </dl>

在包含的命名空間範圍內，以獨特且不透明的方式識別此類別的實例。

> [!IMPORTANT]
>
> 為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*
>
> *OrgID* 必須包含受著作權、商標或其他唯一名稱（由定義 **InstanceID** 的商務實體所擁有），或是由可辨識的全域授權單位所指派的註冊識別碼。 此模式類似于架構類別名稱的結構。 此外，若要確保唯一性， **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。 因此， *OrgID* 不能包含冒號 ( '： ' ) 。
>
> *LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。
>
> 如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。
>
> 若為分散式管理工作強制 (DMTF) 定義的實例，則必須搭配 *OrgID* 設定為 CIM 使用模式。

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業的操作狀態，以及這些狀態之間的轉換。

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**新** (2) 


</dt> <dd>

作業從未啟動。

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) 


</dt> <dd>

作業正在從「新增」、「已暫停」或「服務」狀態移至「正在執行」狀態。

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (4) 


</dt> <dd>

工作正在執行。

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (5) 


</dt> <dd>

作業已停止，但可以順暢的方式重新開機。

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (6) 


</dt> <dd>

作業正在移至「已完成」、「已終止」或「已終止」狀態。

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (7) 


</dt> <dd>

作業已正常完成。

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**終止** (8) 


</dt> <dd>

作業已由「終止」狀態變更要求停止。 作業和其所有基礎進程都已結束，而且可以重新開機 (這只是做為新工作的工作專屬) 。

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>已 **終止** (9) 


</dt> <dd>

作業已由 ' Kill ' 狀態變更要求停止。 基礎進程可能已在執行中，而且可能需要清除才能釋出資源。

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**例外** 狀況 (10) 


</dt> <dd>

作業處於異常狀態，可能表示發生錯誤狀況。 實際狀態可能會顯示在工作特定的物件。

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**服務** (11) 


</dt> <dd>

作業處於支援問題探索、解決或兩者的廠商特定狀態

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**查詢暫** 止 (12) 


</dt> <dd>

等候用戶端解析查詢。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (13. 32767) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 
</dt> </dl>

實例的使用者易記名稱。 此外，使用者易記名稱可用來做為搜尋或查詢的屬性。

> [!Note]  
> 名稱在命名空間中不一定是唯一的。

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

表示已完成的作業保留時間長度。 預設值為 "00000000000500.000000： 000" (五分鐘) 。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次變更工作狀態的日期或時間。

> [!Note]  
> 如果作業的狀態未變更，而且此屬性已填入，則必須將它設定為零間隔值。

 

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

[**CIM \_ 作業**](cim-job.md)
</dt> </dl>

 

