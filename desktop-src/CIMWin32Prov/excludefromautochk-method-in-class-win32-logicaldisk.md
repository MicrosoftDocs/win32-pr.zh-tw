---
description: 排除在下次重新開機時執行的 autochk 作業中的磁片。
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Win32_LogicalDisk 類別的 ExcludeFromAutochk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997065"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Win32 LogicalDisk 類別的 ExcludeFromAutochk 方法 \_

**ExcludeFromAutochk** 方法不會在下次重新開機時，從執行的 **autochk** 作業中排除磁片。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LogicalDisk* \[在\]
</dt> <dd>

下次重新開機時，應從 **autochk** 排除的磁片磁碟機清單。 字串語法是由磁碟機號後面接著邏輯磁片的冒號所組成。

範例： "C："

</dd> </dl>

## <a name="return-value"></a>傳回值

如果沒有發生錯誤，則傳回值為 0 (零) 。 值列在下列清單中。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功** (0) 
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

如果未排除，則會在磁片設定中途位時，在磁片上執行 **autochk** 。 請注意，排除磁片的呼叫不是累計的。 如果進行呼叫以排除某些磁片，則不會將新的清單新增至已標示為排除的磁片清單。 新的磁片清單會覆寫先前的清單。 此方法僅適用于代表電腦中實體磁片的邏輯磁片實例。 它不適用於對應的邏輯磁碟機。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例可確保在下一次電腦重新開機時，Autochk.exe 不會在 C 磁片磁碟機上執行，即使磁片磁碟機 C 上已設定「中途位」也是如此。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
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
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

