---
description: 表示以 AT 命令建立的工作。
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Win32_ScheduledJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025849"
---
# <a name="win32_scheduledjob-class"></a>Win32 \_ register-scheduledjob 類別

**Win32 \_ register-scheduledjob** [WMI 類別](../wmisdk/retrieving-a-class.md)   代表以 **AT** 命令建立的工作。

> [!Note]  
> **Win32 \_ register-scheduledjob** 類別不代表從主控台的排程工作 Wizard 建立的工作。 您無法在 [排程工作] UI 中變更 WMI 所建立的工作。 如需詳細資訊，請參閱＜備註＞一節。

 

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a>成員

**Win32 \_ register-scheduledjob** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ register-scheduledjob** 類別具有這些方法。



| 方法                                                      | 描述                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**創建**](create-method-in-class-win32-scheduledjob.md) | 類別方法，可將作業提交至作業系統，以在指定的未來時間和日期執行。<br/> |
| [**刪除**](delete-method-in-class-win32-scheduledjob.md) | 刪除排程工作的類別方法。<br/>                                                                 |



 

### <a name="properties"></a>屬性

**Win32 \_ register-scheduledjob** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**命令**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**" ) 
</dt> </dl>

命令的名稱、批次程式或二進位檔案 (和命令列引數，) 排程服務用來叫用作業的命令列引數。

範例： "**defrag** **/q/f**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**" ) 
</dt> </dl>

排程執行作業的當月天數。 如果工作排程在一個月的多天執行，這些值可以聯結在邏輯 OR 中。 例如，如果作業是在每個月的1和16執行，則 **DaysOfMonth** 屬性的值會是1或32768。

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1) 


</dt> <dd>

第一

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2) 


</dt> <dd>

第二

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4) 


</dt> <dd>

第三

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8) 


</dt> <dd>

第四

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16) 


</dt> <dd>

第 5 個

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32) 


</dt> <dd>

第 6 個

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64) 


</dt> <dd>

第 7 個

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128) 


</dt> <dd>

第 8 個

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256) 


</dt> <dd>

第 9 個

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512) 


</dt> <dd>

日

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024) 


</dt> <dd>

11th

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048) 


</dt> <dd>

12th

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096) 


</dt> <dd>

13th

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192) 


</dt> <dd>

日

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384) 


</dt> <dd>

日

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768) 


</dt> <dd>

十六

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536) 


</dt> <dd>

17日

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072) 


</dt> <dd>

日前

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144) 


</dt> <dd>

19日

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288) 


</dt> <dd>

月

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576) 


</dt> <dd>

21st

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152) 


</dt> <dd>

22nd

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304) 


</dt> <dd>

23rd

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608) 


</dt> <dd>

24 日

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216) 


</dt> <dd>

百分點

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432) 


</dt> <dd>

26 日

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864) 


</dt> <dd>

27 日

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728) 


</dt> <dd>

28 日

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456) 


</dt> <dd>

29 日

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912) 


</dt> <dd>

號

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824) 


</dt> <dd>

31 日

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**" ) 
</dt> </dl>

排程執行工作的星期幾。 如果工作排程在一周的多天執行，這些值可以聯結在邏輯 OR 中。 例如，如果工作排定在星期一、星期三和星期五執行， **DaysOfWeek** 屬性的值會是1或4或16。

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**星期一** (1) 


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**星期二** (2) 


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**星期三** (4) 


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**星期四** (8) 


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**星期五** (16) 


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**星期六** (32) 


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**星期日** (64) 


</dt> <dd></dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**經過時間**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業已執行的時間長度。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**InteractWithDesktop**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **JOB \_ 非互動式**" ) 
</dt> </dl>

指定的作業是互動式的，這表示使用者可以在執行中的排程工作時提供輸入。

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| \| [**\_ ENUM JobId 的**](/windows/win32/api/lmat/ns-lmat-at_enum)網路管理結構 \| ****" ) 
</dt> </dl>

識別作業的數目。 方法會使用它做為此電腦上所排程之一個作業的控制碼。

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "JobStatus" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( " \| \| [**在 \_ 列舉**](/windows/win32/api/lmat/ns-lmat-at_enum)旗標的 Win32API 網路管理結構 \|  \| **作業 \_ EXEC \_ 錯誤**" ) 
</dt> </dl>

上次排程執行此作業的執行狀態。

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**成功** ( 「成功」 ) 


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**失敗** ( 「失敗」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**通知**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當作業完成或失敗時，使用者會收到通知。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

</dd> <dt>

**擁有者**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提交工作的使用者。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業執行的重要性。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

</dd> <dt>

**RunRepeatedly**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「 \| \| [**在 \_ 資訊**](/windows/win32/api/lmat/ns-lmat-at_info) \| **旗標** \| **工作 \_ \_ 定期執行** Win32API 網路管理結構」 ) 
</dt> </dl>

排程工作會在排定作業的天數重複執行。 如果 **為 False**，則作業會執行一次。

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "StartTime" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**" ) 
</dt> </dl>

執行作業的 UTC 時間，格式為 "YYYYMMDDHHMMSS.FFFFFF"。MMMMMM (+-) OOO "，其中" YYYYMMDD "必須以" "取代 \* \* \* \* \* \* \* \* 。 取代是必要的，因為排程服務只允許將作業設定為執行一次，或在一個月或一周的某一天執行。 無法在特定日期執行作業。

**StartTime** 屬性值的 " (+-) OOO" 區段是本地時間轉譯目前的偏差。 偏差是 UTC 時間與本地時間之間的差異。 若要計算時區的偏差，請將您時區提前或晚于格林威治標準時間的小時數乘以60的 (GMT)  (如果您的時區是在 GMT 之前，則以小時為單位，如果您的時區晚于 gmt) ，則為負數。 如果您的時區使用日光節約時間，請在您的計算中加入額外的60。 例如，太平洋標準時區是 GMT 後八小時，因此偏差等於-420 (-8 \* 60 + 60) 當日光節約時間正在使用中時，當日光節約時間未使用時，則為-480 (-8 \* 60) 。 您也可以藉由查詢 [**Win32 \_ 時區**](win32-timezone.md) 類別的偏差屬性來判斷偏差的值。

例如： " \* \* \* \* \* \* \* \* 123000.000000-420" 會指定 14.30 (2:30 P.M. ) PST，並有日光節約時間生效。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
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

**TimeSubmitted**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提交作業的時間。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業無效或應該停止的時間。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

</dd> </dl>

## <a name="remarks"></a>備註

針對排程服務排程的每個作業都會持續儲存 (排程器可以在重新開機) 之後啟動作業，並在一周或每個月的指定時間執行。 如果電腦不在使用中，或排程服務未在指定的工作時間執行，則排程服務會在下一天的指定時間執行指定的工作。

工作的排程是根據國際標準時間 (UTC) 加上格林威治標準時間 (GMT) 的偏差位移，這表示可以使用任何時區來指定作業。 在列舉物件時， **Win32 \_ register-scheduledjob** 類別會傳回 UTC 位移的當地時間，並在建立新的作業時轉換為當地時間。 例如，指定要在波士頓的電腦上于下午10:30 執行的工作 星期一 PST time 將排程在本機上午1:30 執行。 星期二 EST

> [!Note]  
> 用戶端必須考慮日光節約時間是否在本機電腦上運作，如果是，則從 UTC 位移減去60分鐘的偏差。

 

**Win32 \_ register-scheduledjob** 類別衍生自 [**CIM \_ 工作**](cim-job.md)。 您必須是 administrators 群組的成員，才能使用這個類別建立排程工作。

**Win32 \_ register-scheduledjob** 類別是在內部使用 AT 通訊協定，其系結至從 Windows 8 和 Windows Server 2012 開始的淘汰。 第一個步驟是預設停用的通訊協定。 如果停用通訊協定，例如在 **Win32 \_ register-scheduledjob** 物件上呼叫 [**Create**](create-method-in-class-win32-scheduledjob.md)方法將會失敗，並出現錯誤0x8。 您可以藉由新增下列登錄專案，重新開啟 AT 通訊協定：

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

您可能需要重新開機電腦，才能使設定生效。

因為 **win32 \_ register-scheduledjob** 是以 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) win32 API 為基礎，所以您無法搭配工作排程器使用這個類別。 如果您想要使用工作排程器，請使用工作排程器 API。 如需詳細資訊，請參閱 [工作排程器參考](../taskschd/task-scheduler-reference.md)。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會排程 Notepad.exe 在每個星期三的本機電腦時間以互動的方式在1:25 執行。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



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

[**CIM \_ 作業**](cim-job.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> <dt>

[WMI 工作：已排程的工作](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
