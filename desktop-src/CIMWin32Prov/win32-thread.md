---
description: Win32 \_ 執行緒&\# 8194;WMI 類別代表執行的執行緒。
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Win32_Thread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f3add3a93cc974c2d6c5b20c360d099d46b688887f81cb646005568240a7cb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416714"
---
# <a name="win32_thread-class"></a>Win32 \_ 執行緒類別

**Win32 \_ 執行緒** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行的執行緒。 雖然進程必須有一個執行中的執行緒，但是進程可以建立其他執行緒，以平行方式執行工作。 執行緒共用進程環境，因此同一個進程下的多個執行緒所使用的記憶體會比相同數目的進程更少。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a>成員

**Win32 \_ 執行緒** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ 執行緒** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Cim \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**CSCreationClassName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍電腦系統的建立類別名稱。

這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**CSName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍電腦系統的名稱。

這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**經過時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Performance Data 結構 Performance \| [**\_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) 
</dt> </dl>

自建立之後，提供給這個執行緒的總執行時間（以毫秒為單位）。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

執行緒的目前操作狀況。

這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

**就緒** (2) 


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**正在** 執行 (3) 


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

**封鎖** (4) 


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

**擱置** 的已封鎖 (5) 


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

已 **暫止就緒** (6) 


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ，覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Handle" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Tool Help 結構 \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID" ) 
</dt> </dl>

執行緒的控制碼。 控制碼預設具有完整存取權限。 使用正確的安全性存取時，控制碼可用於接受執行緒控制碼的任何函數。 根據建立時所指定的繼承旗標，這個控制碼可由子進程繼承。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

已安裝物件。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "KernelModeTime" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 效能資料結構效能 \| [**\_ 物件 \_ 類型**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PrivilegedTime" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) 
</dt> </dl>

在核心模式中的時間，以100毫微秒單位表示。 如果無法使用這項資訊，則應使用 0 (零) 的值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**OSCreationClassName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍作業系統的建立類別名稱。

這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**OSName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍作業系統的名稱。

這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Priority" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Tool Help 結構 \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri" ) 
</dt> </dl>

執行緒的動態優先權。 每個執行緒都有動態優先權，讓排程器用來判斷要執行的執行緒。 一開始，執行緒的動態優先權與其基底優先權相同。 系統可以提高和降低動態優先順序，以確保它的回應速度 (保證不會耗盡處理器時間) 的執行緒。 系統不會提高基底優先權層級介於16到31之間的執行緒優先順序。 只有基底優先順序介於0和15之間的執行緒才能獲得動態優先權。 數位愈高表示優先順序較高。

</dd> <dt>

**PriorityBase**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Performance Data 結構 Performance \| [**\_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfPriorityBase" ) 
</dt> </dl>

執行緒的目前基本優先權。 如果執行緒正在處理使用者輸入，作業系統可能會將執行緒的動態優先順序提高到基底優先順序以上，如果執行緒變成計算系結，則會將它降低到基底優先順序。 **PriorityBase** 屬性可以有0到31之間的值。

</dd> <dt>

**ProcessCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**CreationClassName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

範圍處理常式 **CreationClassName** 屬性的值。

這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。

</dd> <dt>

**ProcessHandle**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ，覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "ProcessHandle" ) ，[**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**處理**") ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" Win32API \| Tool Help 結構 \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ") 
</dt> </dl>

建立執行緒的進程。 您可以 Windows 應用程式開發介面 (API) 元素來使用這個屬性的內容。

</dd> <dt>

**StartAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WIn32API \| Thread Object \| LPTHREAD \_ START \_ 常式 \| lpStartAddress" ) 
</dt> </dl>

執行緒的起始位址。 由於具有適當存取執行緒的任何應用程式都可以變更執行緒的內容，因此這個值可能只是執行緒起始位址的近似值。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

值如下：

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

**ThreadState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Thread State" ) 
</dt> </dl>

執行緒的目前執行狀態。

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**初始化** (0) 


</dt> <dd>

已初始化-種微核心可辨識它。

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**就緒** (1) 


</dt> <dd>

就緒—準備好在下一個可用的處理器上執行。

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (2) 


</dt> <dd>

正在執行中-正在執行。

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**待命** (3) 


</dt> <dd>

待命-即將執行，一次只能有一個執行緒處於此狀態。

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>已 **終止** (4) 


</dt> <dd>

已終止-它已完成執行。

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**正在等候** (5) 


</dt> <dd>

等候中-它尚未準備好供處理器進行，將會重新排定。

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**轉換** (6) 


</dt> <dd>

轉換—執行緒正在等候處理器以外的資源，

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (7) 


</dt> <dd>

未知-執行緒狀態不明。

</dd> </dl>

</dd> <dt>

**ThreadWaitReason**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Thread Wait Reason" ) 
</dt> </dl>

執行緒正在等候的原因。 只有當 **ThreadState** 成員設定為轉換 (6) 時，此值才有效。 事件配對允許與受保護子系統進行通訊。

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**主管** (0) 


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1) 


</dt> <dd>

FreePage

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2) 


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3) 


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4) 


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5) 


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6) 


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7) 


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8) 


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9) 


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10) 


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11) 


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12) 


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13) 


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14) 


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15) 


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16) 


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17) 


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18) 


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (20) 


</dt> <dd></dd> </dl>

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "UserModeTime" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 效能資料結構效能 \| [**\_ 物件 \_ 類型**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) 
</dt> </dl>

在使用者模式下的時間，以100毫微秒單位表示。 如果無法使用這項資訊，則應使用 0 (零) 的值。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 執行緒** 類別衍生自 [**CIM \_ 執行緒**](cim-thread.md)。

**概觀**

針對例行的日常監視，通常會有很多原因會有詳細的執行緒清單及其相關聯的屬性。 電腦會在一天中建立及刪除上千個執行緒，而且這些建立或刪除動作對撰寫軟體的開發人員而言有意義。

但是，當您針對應用程式的問題進行疑難排解時，追蹤進程的個別執行緒可讓您識別建立執行緒的時間，以及在 (時或) 終結的時機。 因為建立但未終結的執行緒會造成記憶體流失，所以追蹤個別執行緒可能是支援技術人員的實用資訊。 同樣地，識別執行緒優先順序有助於找出以異常高優先順序執行的執行緒，這是其他執行緒和其他進程所需的優先 CPU 週期。

**使用 Win32 \_ 執行緒**

如同上述語法區塊所暗示， **Win32 \_ 執行緒** 類別不會報告每個執行緒執行時所用的進程名稱。 相反地，它會報告執行緒執行時所用的進程識別碼。 若要傳回進程的名稱和其所有線程的清單，您的腳本必須：

1.  連線至 [**Win32 \_ 進程**](win32-process.md)類別，並傳回進程及其處理序識別碼的清單。
2.  將此資訊暫時儲存在陣列或字典物件中。
3.  針對每個處理序識別碼，傳回該進程的執行緒清單，然後顯示進程名稱和執行緒清單。

## <a name="examples"></a>範例

下列 VBScript 範例會監視電腦上執行的執行緒。


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
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

[**CIM \_ 執行緒**](cim-thread.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
