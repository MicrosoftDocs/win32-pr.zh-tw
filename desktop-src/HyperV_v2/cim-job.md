---
description: 代表要執行之工作單位（例如腳本或列印工作）的邏輯元素。 作業與進程不同，因為作業可以排程或排入佇列，而且其執行不限於單一系統。
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: 'CIM_Job 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8eb8f63ec9d2cdd881a2ba0946f83a40fb8be866
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474584"
---
# <a name="cim_job-class-hyper-v-management"></a>CIM_Job 類別 (Hyper-v 管理) 

代表要執行之工作單位（例如腳本或列印工作）的邏輯元素。 作業與進程不同，因為作業可以排程或排入佇列，而且其執行不限於單一系統。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a>成員

**CIM \_ 作業** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ 作業** 類別具有這些方法。




| 方法 | 描述 | 
|--------|-------------|
| <a href="cim-job-killjob.md"><strong>KillJob</strong></a> | 此方法已被取代。 請改用 <strong>RequestStateChange</strong> 方法。<br /><blockquote>[!Note]<br />已淘汰的描述：關閉作業。</blockquote><br /> | 




 

### <a name="properties"></a>屬性

**CIM \_ 作業** 類別具有這些屬性。

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

**True** 表示在完成時刪除作業;否則 **為 false**。

> [!Note]  
> 這個屬性不會刪除此屬性設定為 **True** 之前完成的工作。

 

</dd> <dt>

**經過時間**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業已執行的持續時間。

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**ErrorDescription**") 
</dt> </dl>

特定廠商的錯誤碼，可捕獲週期性作業的處理資訊。 如果作業已完成而沒有錯誤，則值必須設為零。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**ErrorCode**") 
</dt> </dl>

自由格式的字串，其中包含 **ErrorCode** 屬性中對應錯誤碼的描述。

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

作業的執行次數。

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**") 
</dt> </dl>

表示作業狀態的自由格式字串。

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出 **RunStartInterval** 和 **UntilTime** 屬性中的時間是否代表當地時間或 UTC 時間。

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

**本地時間** (1) 


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

**UTC 時間** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**通知**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

當作業完成或失敗時要通知的使用者。

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RecoveryAction**") 
</dt> </dl>

描述 **RecoveryAction** 屬性為 **其他** ( "1" ) 時之復原動作的字串。

</dd> <dt>

**擁有者**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ OwningJobElement**](cim-owningjobelement.md)」。) 
</dt> </dl>

提交作業的使用者，或要求作業的服務或方法名稱。

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "percent" ) ， [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ， [**Timespan.maxvalue**](/windows/desktop/WmiSdk/standard-qualifiers) (101) ， **PUnit** ( "percent" ) 
</dt> </dl>

完成的作業百分比。

> [!Note]  
> 值 "101" 未定義，將不會在規格的下一個主要修訂中允許。

 

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

工作的重要性。 編號愈低，優先順序愈高。

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**OtherRecoveryAction**") 
</dt> </dl>

描述執行作業失敗時要採取的修復動作。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

什麼是要採取的復原動作未知。

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

復原動作將會在 **OtherRecoveryAction** 屬性中指定。

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**請勿繼續** (2) 


</dt> <dd>

停止執行作業，並適當地更新其狀態。

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**繼續進行下一個工作** (3) 


</dt> <dd>

繼續執行佇列中的下一個工作。

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span> (4) **重新執行作業**


</dt> <dd>

應重新執行作業。

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**執行復原工作** (5) 


</dt> <dd>

執行使用 **RecoveryJob** 關聯性建立關聯的作業。 請注意，復原工作必須已在將執行它的佇列中。

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31) ， [**int32.maxvalue (31**](/windows/desktop/WmiSdk/standard-qualifiers)) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") 
</dt> </dl>

搭配 **RunDayOfWeek** 屬性使用的整數，表示處理作業的日期;或者，如果 **RunDayOfWeek** 設定為零，則 **RunDay** 會指出處理作業的月份日期。 如果 **RunDay** 是負整數，它會指定相對於月底的一天，或如果 **RunDay** 是正整數，則會指定一天相對於當月的開始時間。

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

資料類型： **sint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDay**"，"**CIM \_ 作業**。**RunStartInterval**") 
</dt> </dl>

搭配 **RunDay** 屬性使用的整數，表示處理作業的日期;或者，如果 **RunDayOfWeek** 設定為零，則 **RunDay** 會指出處理作業的月份日期。

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-星期六** (-7) 


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-星期五** (-6) 


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-星期四** (-5) 


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-星期三** (-4) 


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-星期二** (-3) 


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-星期一** (-2) 


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-星期日** (-1) 


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**ExactDayOfMonth** (0) 


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**星期日** (1) 


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**星期一** (2) 


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**星期二** (3) 


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**星期三** (4) 


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**星期四** (5) 


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**星期五** (6) 


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**星期六** (7) 


</dt> <dd></dd> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunDay**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") 
</dt> </dl>

處理作業的月份。

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**1 月** (0) 


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**二月** (1) 


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**3 月** (2) 


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**四月** (3) 


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**5 月** (4) 


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**6 月** (5) 


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**7 月** (6) 


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**8 月** (7) 


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**9 月** (8) 


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**10 月** (9) 


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**11 月** (10) 


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**12 月** (11) 


</dt> <dd></dd> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDay**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") 
</dt> </dl>

處理作業的午夜之後的時間間隔。 例如，"00000000020000.000000： 000" 表示作業是在兩個點鐘的當地時間或之後執行，或 UTC 時間 (UTC 是以 **LocalOrUtcTime** 屬性) 指定。

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDay**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") 
</dt> </dl>

> [!Note]  
> 此屬性已被取代。 建議您改用 **RunMonth**、 **RunDay**、 **RunDayOfWeek** 和 **RunStartInterval** 屬性。

 

排程目前作業開始的時間。 這段時間可由日期和時程表示，或以相對於要求屬性時間的間隔來表示。 全部為零的值表示作業已在執行中。

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業開始的時間。 這段時間可由日期和時程表示，或以相對於要求屬性時間的間隔來表示。

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提交作業的時間。 全部為零的值表示父項目不能報告日期和時間。

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**LocalOrUtcTime**") 
</dt> </dl>

作業變成無效或應該停止的時間。 時間可以用日期和時程表示，或以相對於要求此屬性時間的間隔來表示。 所有九的值表示作業可以無限期執行。

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

 

