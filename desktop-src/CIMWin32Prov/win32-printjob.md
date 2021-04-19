---
description: 代表 Windows 應用程式所產生的列印工作。 在 Windows 作業系統上執行之電腦上執行之應用程式的 [列印] 命令所產生的任何工作單位，都是此類別的子系或成員。
ms.assetid: d884acba-e1b2-4d24-9b55-15d175a163d9
ms.tgt_platform: multiple
title: Win32_PrintJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob
- Win32_PrintJob.Caption
- Win32_PrintJob.Description
- Win32_PrintJob.InstallDate
- Win32_PrintJob.Name
- Win32_PrintJob.Status
- Win32_PrintJob.ElapsedTime
- Win32_PrintJob.JobStatus
- Win32_PrintJob.Notify
- Win32_PrintJob.Owner
- Win32_PrintJob.Priority
- Win32_PrintJob.StartTime
- Win32_PrintJob.TimeSubmitted
- Win32_PrintJob.UntilTime
- Win32_PrintJob.Color
- Win32_PrintJob.DataType
- Win32_PrintJob.Document
- Win32_PrintJob.DriverName
- Win32_PrintJob.HostPrintQueue
- Win32_PrintJob.JobId
- Win32_PrintJob.PagesPrinted
- Win32_PrintJob.PaperLength
- Win32_PrintJob.PaperSize
- Win32_PrintJob.PaperWidth
- Win32_PrintJob.Parameters
- Win32_PrintJob.PrintProcessor
- Win32_PrintJob.Size
- Win32_PrintJob.StatusMask
- Win32_PrintJob.TotalPages
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f56034161a9313eed1b7d302ab790d153c0ee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989899"
---
# <a name="win32_printjob-class"></a>Win32 \_ PrintJob 類別

**Win32 \_ PrintJob** [WMI 類別](../wmisdk/retrieving-a-class.md)代表 Windows 應用程式所產生的列印工作。 在 Windows 作業系統上執行之電腦上執行之應用程式的 [列印] 命令所產生的任何工作單位，都是此類別的子系或成員。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class Win32_PrintJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Color;
  string   DataType;
  string   Document;
  string   DriverName;
  string   HostPrintQueue;
  uint32   JobId;
  uint32   PagesPrinted;
  uint32   PaperLength;
  string   PaperSize;
  uint32   PaperWidth;
  string   Parameters;
  string   PrintProcessor;
  uint32   Size;
  uint32   StatusMask;
  uint32   TotalPages;
};
```

## <a name="members"></a>成員

**Win32 \_ PrintJob** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ PrintJob** 類別具有這些方法。



| 方法                                                  | 描述                       |
|:--------------------------------------------------------|:----------------------------------|
| [**暫停**](pause-method-in-class-win32-printjob.md)   | 暫停列印工作。<br/>    |
| [**繼續**](resume-method-in-class-win32-printjob.md) | 繼續進行列印工作。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ PrintJob** 類別具有這些屬性。

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

**色彩**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檔是否以色彩或單色列印的字串。 有些彩色印表機可以使用黑色黑色，而非使用黃色、青色和洋紅的組合來列印。 True 黑色通常會為檔建立深色且更清晰的文字。 此選項僅適用于支援真黑色列印的彩色印表機。

值如下：

<dl><span id="_Color_"></span><span id="_color_"></span><span id="_COLOR_"></span><dt>

**色彩**
</dt><span id="_Monochrome_"></span><span id="_monochrome_"></span><span id="_MONOCHROME_"></span><dt>

**單色**
</dt> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這項列印工作的資料格式。 這會指示印表機驅動程式將資料轉譯 (一般文字、PostScript 或 PCL) ，然後再列印，或以原始格式 (針對圖形和圖片) 進行列印。

範例：「文字」

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

**文件**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列印工作的名稱。 當您在觀看等候列印的檔時，使用者會看到這個名稱。

範例： "Microsoft Word-Review.doc"

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用於列印工作的印表機驅動程式名稱。

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

**HostPrintQueue**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立列印工作的電腦名稱稱。

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

**JobId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業的識別碼。 其他方法會使用它做為印表機的作業幕後處理的控制碼。

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示作業狀態的自由格式字串。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

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

**PagesPrinted**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列印的頁面數目。 如果列印工作未包含頁面分隔資訊，則此值可能是 0 (零) 。

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (十分之一. ) 
</dt> </dl>

紙張的長度。

範例：2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來列印工作的紙張大小。 此值是 [**Win32 \_ 印表機**](win32-printer.md)類別的 **PaperSizesSupported** 屬性中所指定印表機的其中一種可能紙張大小。

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (十分之一. ) 
</dt> </dl>

紙張的寬度。

範例：2159

</dd> <dt>

**參數**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要傳送至列印處理器的選擇性參數。 如需詳細資訊，請參閱 **PrintProcessor** 屬性。

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來處理列印工作的列印處理器服務。 印表機處理器會與印表機驅動程式搭配使用，為印表機提供印表機資料的額外轉譯，也可以用來提供特殊選項，例如作業的封面頁。

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

**大小**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](../wmisdk/standard-qualifiers.md) (位元組) 
</dt> </dl>

列印工作的大小。

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

作業開始的時間。

這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。

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

**StatusMask**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與此列印工作相關之可能狀態的點陣圖。

<dt>

1 (0x1) 
</dt> <dd>

已暫停

</dd> <dt>

2 (0x2) 
</dt> <dd>

錯誤

</dd> <dt>

4 (0x4) 
</dt> <dd>

刪除

</dd> <dt>

8 (0x8) 
</dt> <dd>

假 離線

</dd> <dt>

16 (0x10) 
</dt> <dd>

列印

</dd> <dt>

32 (0x20) 
</dt> <dd>

離線

</dd> <dt>

64 (0x40) 
</dt> <dd>

Paperout

</dd> <dt>

128 (0x80) 
</dt> <dd>

印刷

</dd> <dt>

256 (0x100)
</dt> <dd>

已刪除

</dd> <dt>

512 (0x200) 
</dt> <dd>

封鎖的 \_ DevQ

</dd> <dt>

1024 (0x400) 
</dt> <dd>

使用者 \_ 介入 \_ 需求

</dd> <dt>

2048 (0x800) 
</dt> <dd>

重新啟動

</dd> </dl>

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

**TotalPages**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

完成工作所需的頁面數目。 如果列印工作未包含頁面分隔資訊，則此值可能是 0 (零) 。

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

**Win32 \_ PrintJob** 類別衍生自 [**CIM \_ 工作**](cim-job.md)。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例說明如何從 **Win32 \_ PrintJob** 的實例中取出印表機作業統計資料。


```VB
Set PrintJobSet = GetObject("winmgmts:").InstancesOf ("Win32_PrintJob")

If (PrintJobSet.Count = 0) Then WScript.Echo "No print jobs!"
for each PrintJob in PrintJobSet
 WScript.Echo PrintJob.Name
 WScript.Echo PrintJob.JobId
 WScript.Echo PrintJob.Status
 WScript.Echo PrintJob.TotalPages
 Wscript.Echo ""
next
```



下列 Perl 程式碼範例說明如何從 **Win32 \_ PrintJob** 的實例中取出印表機作業統計資料。


```
use strict;
use Win32::OLE;

close (STDERR);

my ($PrintJobset, $PrintJob);
eval {$PrintJobset = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 InstancesOf ("Win32_PrintJob") };
if (!$@ && defined $PrintJobset)
{
 if ($PrintJobset->{Count} == 0 ) 
 {
  print "\nNo print jobs!\n";
 }

 foreach $PrintJob (in $PrintJobset)
 {
  print $PrintJob->{Name} , "\n";
  print $PrintJob->{JobId} , "\n";
  print $PrintJob->{Status} , "\n";
  print $PrintJob->{TotalPages} , "\n";
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 作業**](./cim-job.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
