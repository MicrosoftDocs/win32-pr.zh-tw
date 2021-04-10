---
description: 排程在下次重新開機時，于 Win32 LogicalDisk 所代表的磁片磁碟機上執行的 Autochk （ \_ 如果已設定中途位）。
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Win32_LogicalDisk 類別的 ScheduleAutoChk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936175"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Win32 LogicalDisk 類別的 ScheduleAutoChk 方法 \_

如果設定了中途的位， **ScheduleAutoChk** 類別方法會排程在下次重新開機時，于 [**Win32 \_ LogicalDisk**](win32-logicaldisk.md) 所代表的磁片磁碟機上執行 Autochk。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LogicalDisk* \[在\]
</dt> <dd>

指定下次重新開機時要針對 Autochk 排程的磁片磁碟機清單。 字串語法是由磁碟機號後面接著邏輯磁片的冒號所組成，例如： "C："

> [!Note]  
> 當資料來自不明來源或您不信任的來源時，請一律檢查 *LogicalDisk* 陣列中的磁碟機號有效性。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回值為 0 (零) ，如果發生任何其他錯誤，則傳回其他值。 值列在下列清單中。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**沒有錯誤** (0) 
</dt> <dt>

**錯誤-遠端磁片磁碟機** (1) 
</dt> <dt>

**錯誤-抽取式磁碟** 機 (2) 
</dt> <dt>

**錯誤-磁片磁碟機不是根目錄** (3) 
</dt> <dt>

**錯誤-未知的磁片磁碟機** (4) 
</dt> </dl>

## <a name="remarks"></a>備註

此方法僅適用于代表電腦中實體磁片的邏輯磁片實例。 這個方法不適用於對應的邏輯磁碟機。

## <a name="examples"></a>範例

下列 VBScript 和 PowerShell 範例會排程 Autochk.exe 下次電腦重新開機時，對 C 磁片磁碟機執行。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
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

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> </dl>

 

