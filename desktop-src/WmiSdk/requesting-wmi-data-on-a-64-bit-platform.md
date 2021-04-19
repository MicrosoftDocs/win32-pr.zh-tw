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
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="a124c-103">在64位平臺上要求 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="a124c-103">Requesting WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="a124c-104">根據預設，當有兩個版本的提供者時，應用程式或腳本會接收來自對應提供者的資料。</span><span class="sxs-lookup"><span data-stu-id="a124c-104">By default, an application or script receives data from the corresponding provider when two versions of providers exist.</span></span> <span data-ttu-id="a124c-105">32位提供者會將資料傳回至32位應用程式（包括所有腳本），而64位提供者則會將資料傳回至64位編譯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a124c-105">The 32-bit provider returns data to a 32-bit application, including all scripts, and the 64-bit provider returns data to the 64-bit compiled applications.</span></span> <span data-ttu-id="a124c-106">不過，應用程式或腳本可以從非預設提供者要求資料（如果存在的話），方法是透過方法呼叫上的旗標來通知 WMI。</span><span class="sxs-lookup"><span data-stu-id="a124c-106">However, an application or script can request data from the nondefault provider, if it exists, by notifying WMI through flags on method calls.</span></span>

## <a name="context-flags"></a><span data-ttu-id="a124c-107">內容旗標</span><span class="sxs-lookup"><span data-stu-id="a124c-107">Context Flags</span></span>

<span data-ttu-id="a124c-108">**\_ \_ Microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 和 **\_ \_ RequiredArchitecture** 字串旗標有一組由 WMI 處理但未在 SDK 標頭或類型程式庫檔案中定義的值。</span><span class="sxs-lookup"><span data-stu-id="a124c-108">The **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** string flags have a set of values handled by WMI but not defined in SDK header or type library files.</span></span> <span data-ttu-id="a124c-109">這些值會放在內容參數中，以通知 WMI 它應該從非預設提供者要求資料。</span><span class="sxs-lookup"><span data-stu-id="a124c-109">The values are placed in a context parameter to signal WMI that it should request data from the nondefault provider.</span></span>

<span data-ttu-id="a124c-110">以下列出旗標及其可能的值。</span><span class="sxs-lookup"><span data-stu-id="a124c-110">The following lists the flags and their possible values.</span></span>

<dl> <dt>

<span data-ttu-id="a124c-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_Microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<**</span><span class="sxs-lookup"><span data-stu-id="a124c-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="a124c-112">指定32位或64位版本的整數值（32或64）。</span><span class="sxs-lookup"><span data-stu-id="a124c-112">Integer value, either 32 or 64, that specifies the 32-bit or 64-bit version.</span></span>

</dd> <dt>

<span data-ttu-id="a124c-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span><span class="sxs-lookup"><span data-stu-id="a124c-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="a124c-114">除了 **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 之外，還會使用布林值來強制載入指定的提供者版本。</span><span class="sxs-lookup"><span data-stu-id="a124c-114">Boolean value used in addition to **\_\_ProviderArchitecture** to force load the specified provider version.</span></span> <span data-ttu-id="a124c-115">如果版本無法使用，則 WMI 會傳回錯誤0x80041013、 **wbemErrProviderLoadFailure** （適用于 Visual Basic）和 **WBEM \_ E \_ 提供者 \_ 載入 \_ 失敗** （c + +）。</span><span class="sxs-lookup"><span data-stu-id="a124c-115">If the version is unavailable, then WMI returns the error 0x80041013, **wbemErrProviderLoadFailure** for Visual Basic and **WBEM\_E\_PROVIDER\_LOAD\_FAILURE** for C++.</span></span> <span data-ttu-id="a124c-116">未指定時，此旗標的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a124c-116">The default value for this flag when it is not specified is **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="a124c-117">在具有並存版本的提供者的64位系統上，除非提供這些旗標，並指出應該傳回64位提供者資料，否則32位應用程式或腳本會自動接收來自32位提供者的資料。</span><span class="sxs-lookup"><span data-stu-id="a124c-117">On a 64-bit system that has side-by-side versions of a provider, a 32-bit application or script automatically receives data from the 32-bit provider, unless these flags are supplied and indicate that the 64-bit provider data should be returned.</span></span>

## <a name="using-the-context-flags"></a><span data-ttu-id="a124c-118">使用內容旗標</span><span class="sxs-lookup"><span data-stu-id="a124c-118">Using the Context Flags</span></span>

<span data-ttu-id="a124c-119">C + + 應用程式可以使用 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 介面搭配 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ，將非預設提供者的使用方式傳達給 WMI。</span><span class="sxs-lookup"><span data-stu-id="a124c-119">C++ applications can use the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface with [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to communicate the use of a nondefault provider to WMI.</span></span>

<span data-ttu-id="a124c-120">在腳本和 Visual Basic 中，您必須建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，其中包含 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)之 *objWbemNamedValueSet* 參數的旗標。</span><span class="sxs-lookup"><span data-stu-id="a124c-120">In scripting and Visual Basic, you must create a [**SWbemNamedValueSet**](swbemnamedvalueset.md) object containing the flags for the *objWbemNamedValueSet* parameter of [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="a124c-121">如需有關為此呼叫設定參數物件的詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="a124c-121">For more information about setting up the parameters objects for this call, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="a124c-122">您可以使用較舊的作業系統中的內容旗標安全地執行腳本和應用程式，因為 WMI 會在未執行這些作業的系統中加以忽略。</span><span class="sxs-lookup"><span data-stu-id="a124c-122">You can safely run scripts and applications using the context flags in older operating systems, because WMI ignores them in systems in which they are not implemented.</span></span> <span data-ttu-id="a124c-123">雖然 System Registry 提供者的32位和64位版本存在，但請注意，只有一個版本的 WMI 存放庫存在。</span><span class="sxs-lookup"><span data-stu-id="a124c-123">While 32-bit and 64-bit versions of the System Registry provider exist, note that only one version of the WMI repository exists.</span></span>

## <a name="accessing-the-default-registry-hive"></a><span data-ttu-id="a124c-124">存取預設登錄 Hive</span><span class="sxs-lookup"><span data-stu-id="a124c-124">Accessing the Default Registry Hive</span></span>

<span data-ttu-id="a124c-125">下列一系列的範例會使用登錄 [提供者，該提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)在64位作業系統上預先安裝了並存的32位和64位版本。</span><span class="sxs-lookup"><span data-stu-id="a124c-125">The following series of examples use the [Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which has side-by-side 32-bit and 64-bit versions preinstalled on 64-bit operating systems.</span></span> <span data-ttu-id="a124c-126">在這些範例中，32位用戶端會從32位節點取得提供者傳回的資料 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Wow6432Node \\ Microsoft**。</span><span class="sxs-lookup"><span data-stu-id="a124c-126">In these examples, 32-bit clients get data returned by the provider from the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft**.</span></span> <span data-ttu-id="a124c-127">64位用戶端從64位節點取得提供者傳回的資料 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 記錄**。</span><span class="sxs-lookup"><span data-stu-id="a124c-127">64-bit clients get data returned by the provider from the 64-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Logging**.</span></span>

<span data-ttu-id="a124c-128">腳本會示範如何透過 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)呼叫登錄 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)類別的方法，以取得32位登錄區中的資料。</span><span class="sxs-lookup"><span data-stu-id="a124c-128">The scripts show how to call the methods of the Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class through [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to obtain data from the 32-bit registry hive.</span></span>

<span data-ttu-id="a124c-129">下列腳本會從提供者取得符合呼叫端位寬度的提供者（在此案例中為64位），因為它是在64位 Windows 腳本主機下執行的腳本 (WSH) 。</span><span class="sxs-lookup"><span data-stu-id="a124c-129">The following script gets back data from the provider that matches the bit width of the caller, in this case 64 bits, because it is a script running under the 64-bit Windows Script Host (WSH).</span></span> <span data-ttu-id="a124c-130">此腳本會從64位登錄節點取得值 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ wbem \\ cimom \\ 記錄** ，而不是32位節點 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Wow6432Node \\ Microsoft \\ WBEM \\ cimom**。</span><span class="sxs-lookup"><span data-stu-id="a124c-130">The script gets the value from the 64-bit registry node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM\\Logging** rather than the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\WBEM\\CIMOM**.</span></span>


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



<span data-ttu-id="a124c-131">如果預設 hive 中的 **記錄** 值設定為1，則腳本的輸出看起來應該會像下面這樣：</span><span class="sxs-lookup"><span data-stu-id="a124c-131">If the **Logging** value in the default hive is set to 1, then the output from the script should look something like the following:</span></span>

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="a124c-132">範例：在64位電腦上特別要求32位登錄 Hive</span><span class="sxs-lookup"><span data-stu-id="a124c-132">Example: Specifically Requesting the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="a124c-133">下列修改過的預設腳本範例會使用 **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 字串旗標，要求在64位電腦上存取32位的登錄資料。</span><span class="sxs-lookup"><span data-stu-id="a124c-133">The following modified example of the default script uses the **\_\_ProviderArchitecture** string flag to request access to the 32-bit registry data on a 64-bit computer.</span></span> <span data-ttu-id="a124c-134">無論是32或64位應用程式，呼叫端都會連接至32位的 hive。</span><span class="sxs-lookup"><span data-stu-id="a124c-134">The caller is connected to the 32-bit hive irrespective of whether it is a 32- or 64-bit application.</span></span>


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



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="a124c-135">範例：強制 WMI 存取64位電腦上的32位登錄 Hive</span><span class="sxs-lookup"><span data-stu-id="a124c-135">Example: Forcing WMI to Access the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="a124c-136">下列透過將 **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 和 **\_ \_ RequiredArchitecture** 旗標新增至內容參數的腳本修改，會強制 WMI 載入32位提供者並取得32位的資料。</span><span class="sxs-lookup"><span data-stu-id="a124c-136">The following modification of the script above by adding the **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** flags to the context parameter forces WMI to load the 32-bit provider and get 32-bit data.</span></span> <span data-ttu-id="a124c-137">如果提供者不存在，就會發生提供者載入錯誤。</span><span class="sxs-lookup"><span data-stu-id="a124c-137">If the provider does not exist, then a provider load error occurs.</span></span> <span data-ttu-id="a124c-138">您必須藉由呼叫 [**Wbemscripting.swbemlocator ConnectServer**](swbemlocator-connectserver.md)，在與 WMI 的連接中提供內容物件。</span><span class="sxs-lookup"><span data-stu-id="a124c-138">The context object must be supplied in the connection to WMI by calling [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a124c-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="a124c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a124c-140">在64位電腦上取得和提供資料</span><span class="sxs-lookup"><span data-stu-id="a124c-140">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
