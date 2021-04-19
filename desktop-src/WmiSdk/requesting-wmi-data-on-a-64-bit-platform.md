---
description: 根據預設，當有兩個版本的提供者時，應用程式或腳本會接收來自對應提供者的資料。
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: 在64位平臺上要求 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979066"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>在64位平臺上要求 WMI 資料

根據預設，當有兩個版本的提供者時，應用程式或腳本會接收來自對應提供者的資料。 32位提供者會將資料傳回至32位應用程式（包括所有腳本），而64位提供者則會將資料傳回至64位編譯的應用程式。 不過，應用程式或腳本可以從非預設提供者要求資料（如果存在的話），方法是透過方法呼叫上的旗標來通知 WMI。

## <a name="context-flags"></a>內容旗標

**\_ \_ Microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 和 **\_ \_ RequiredArchitecture** 字串旗標有一組由 WMI 處理但未在 SDK 標頭或類型程式庫檔案中定義的值。 這些值會放在內容參數中，以通知 WMI 它應該從非預設提供者要求資料。

以下列出旗標及其可能的值。

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_Microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<**
</dt> <dd>

指定32位或64位版本的整數值（32或64）。

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**
</dt> <dd>

除了 **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 之外，還會使用布林值來強制載入指定的提供者版本。 如果版本無法使用，則 WMI 會傳回錯誤0x80041013、 **wbemErrProviderLoadFailure** （適用于 Visual Basic）和 **WBEM \_ E \_ 提供者 \_ 載入 \_ 失敗** （c + +）。 未指定時，此旗標的預設值為 **FALSE**。

</dd> </dl>

在具有並存版本的提供者的64位系統上，除非提供這些旗標，並指出應該傳回64位提供者資料，否則32位應用程式或腳本會自動接收來自32位提供者的資料。

## <a name="using-the-context-flags"></a>使用內容旗標

C + + 應用程式可以使用 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 介面搭配 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ，將非預設提供者的使用方式傳達給 WMI。

在腳本和 Visual Basic 中，您必須建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，其中包含 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)之 *objWbemNamedValueSet* 參數的旗標。 如需有關為此呼叫設定參數物件的詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

您可以使用較舊的作業系統中的內容旗標安全地執行腳本和應用程式，因為 WMI 會在未執行這些作業的系統中加以忽略。 雖然 System Registry 提供者的32位和64位版本存在，但請注意，只有一個版本的 WMI 存放庫存在。

## <a name="accessing-the-default-registry-hive"></a>存取預設登錄 Hive

下列一系列的範例會使用登錄 [提供者，該提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)在64位作業系統上預先安裝了並存的32位和64位版本。 在這些範例中，32位用戶端會從32位節點取得提供者傳回的資料 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Wow6432Node \\ Microsoft**。 64位用戶端從64位節點取得提供者傳回的資料 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 記錄**。

腳本會示範如何透過 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)呼叫登錄 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別的方法，以取得32位登錄區中的資料。

下列腳本會從提供者取得符合呼叫端位寬度的提供者（在此案例中為64位），因為它是在64位 Windows 腳本主機下執行的腳本 (WSH) 。 此腳本會從64位登錄節點取得值 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ wbem \\ cimom \\ 記錄** ，而不是32位節點 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Wow6432Node \\ Microsoft \\ WBEM \\ cimom**。


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



如果預設 hive 中的 **記錄** 值設定為1，則腳本的輸出看起來應該會像下面這樣：

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>範例：在64位電腦上特別要求32位登錄 Hive

下列修改過的預設腳本範例會使用 **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 字串旗標，要求在64位電腦上存取32位的登錄資料。 無論是32或64位應用程式，呼叫端都會連接至32位的 hive。


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>範例：強制 WMI 存取64位電腦上的32位登錄 Hive

下列透過將 **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 和 **\_ \_ RequiredArchitecture** 旗標新增至內容參數的腳本修改，會強制 WMI 載入32位提供者並取得32位的資料。 如果提供者不存在，就會發生提供者載入錯誤。 您必須藉由呼叫 [**Wbemscripting.swbemlocator ConnectServer**](swbemlocator-connectserver.md)，在與 WMI 的連接中提供內容物件。


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
