---
description: 建立新的印表機驅動程式。
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Win32_PrinterDriver 類別的 AddPrinterDriver 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385878"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Win32 PrinterDriver 類別的 AddPrinterDriver 方法 \_

**AddPrinterDriver** 類別方法會建立新的印表機驅動程式。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DriverInfo* \[在\]
</dt> <dd>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)類別的實例，代表印表機驅動程式。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 針對不同于下列清單中所列的值，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants)。

<dl> <dt>

**0**
</dt> <dd>

成功。

</dd> <dt>

**5**
</dt> <dd>

拒絕存取。

</dd> <dt>

**87**
</dt> <dd>

參數錯誤。 當物件未正確填滿，或在系統中找不到驅動程式時，可能會發生此問題。 或者，[名稱] 屬性可能與 .inf 檔案中指定的模型不同。 或者，PathFile 屬性上可能會有遺漏的反斜線 ( " \\ " ) 。

</dd> <dt>

**1797**
</dt> <dd>

印表機驅動程式未知。

</dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> 使用 **AddPrinterDriver** 方法時，您必須使用 **SeLoadDriverPrivilege** 來載入或卸載設備磁碟機。

 

## <a name="examples"></a>範例

[[在驅動程式封包中找不到安裝印表機驅動程式](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) ] VBScript 程式碼範例會使用 Drivers.cab 中找不到的列印驅動程式來安裝假設的印表機。

下列 VBScript 範例會安裝 Apple LaserWriter 8500 印表機的印表機驅動程式。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
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

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

