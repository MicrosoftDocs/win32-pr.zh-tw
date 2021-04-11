---
description: 重新命名電腦。
ms.assetid: 9d338ebe-caf0-42c4-995f-fd750e5664df
ms.tgt_platform: multiple
title: Win32_ComputerSystem 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ca60021c921e47de3c7afd5b8ee0bb2ea5e6d12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025827"
---
# <a name="rename-method-of-the-win32_computersystem-class"></a><span data-ttu-id="46760-103">Win32 的 [重新命名] 類別的方法 \_</span><span class="sxs-lookup"><span data-stu-id="46760-103">Rename method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="46760-104">**重新命名** 方法會將電腦重新命名。</span><span class="sxs-lookup"><span data-stu-id="46760-104">The **Rename** method renames a computer.</span></span>

<span data-ttu-id="46760-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="46760-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="46760-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="46760-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="46760-107">語法</span><span class="sxs-lookup"><span data-stu-id="46760-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name,
  [in] string Password,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="46760-108">參數</span><span class="sxs-lookup"><span data-stu-id="46760-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46760-109">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46760-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46760-110">新電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="46760-110">New computer name.</span></span> <span data-ttu-id="46760-111">此參數的值不能包含控制字元、開頭或尾端空格，或下列任何字元：/ \\ \\ \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="46760-111">The value of this parameter cannot include control characters, leading or trailing spaces, or any of the following characters: / \\\\ \[ \].</span></span>

</dd> <dt>

<span data-ttu-id="46760-112">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46760-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46760-113">當 *UserName* 參數指定帳戶名稱時，用來連接到網域控制站的密碼。</span><span class="sxs-lookup"><span data-stu-id="46760-113">Password to use when connecting to the domain controller if the *UserName* parameter specifies an account name.</span></span> <span data-ttu-id="46760-114">否則，此參數必須為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="46760-114">Otherwise, this parameter must be **NULL**.</span></span> <span data-ttu-id="46760-115">如需 *密碼* 和使用者 *名稱* 參數的詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="46760-115">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="46760-116">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46760-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46760-117">字串，指定連接到網域控制站時要使用的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="46760-117">String that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="46760-118">字串必須以 **null** 終止，且必須指定網域 NetBIOS 名稱和使用者帳戶，例如 "DOMAINNAME \\ username" 或 " someone@domainname.com "，這是 (UPN) 的使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="46760-118">The string must be **null**-terminated, and must specify a domain NetBIOS name and user account for example, "DOMAINNAME\\username" or "someone@domainname.com", which is a user principal name (UPN).</span></span> <span data-ttu-id="46760-119">如果 **UserName** 參數為 **Null**，WMI 會使用呼叫端的內容。</span><span class="sxs-lookup"><span data-stu-id="46760-119">If the **UserName** parameter is **NULL**, WMI uses the context of the caller.</span></span> <span data-ttu-id="46760-120">如需 *密碼* 和使用者 *名稱* 參數的詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="46760-120">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46760-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="46760-121">Return value</span></span>

<span data-ttu-id="46760-122">如果成功，則傳回 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="46760-122">Returns a 0 (zero) if successful.</span></span> <span data-ttu-id="46760-123">非零傳回值表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="46760-123">A nonzero return value indicates an error.</span></span> <span data-ttu-id="46760-124">如果成功，則需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="46760-124">If successful, a reboot is required.</span></span> <span data-ttu-id="46760-125">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="46760-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="46760-126">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="46760-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="46760-127">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="46760-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46760-128">**其他** (1 4294967295) </span><span class="sxs-lookup"><span data-stu-id="46760-128">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="46760-129">備註</span><span class="sxs-lookup"><span data-stu-id="46760-129">Remarks</span></span>

<span data-ttu-id="46760-130">如果您是本機系統管理員群組的成員，您可以使用 **重新命名** 方法來重新命名電腦。</span><span class="sxs-lookup"><span data-stu-id="46760-130">You can use the **Rename** method to rename a computer if you are a member of the local administrator group.</span></span> <span data-ttu-id="46760-131">不過，您不能將此方法用於網域電腦的遠端。</span><span class="sxs-lookup"><span data-stu-id="46760-131">However, you cannot use the method remotely for domain computers.</span></span>

<span data-ttu-id="46760-132">如果指定了 *Password* 和 *UserName* 參數，與 WMI 的連線必須使用 **RPC \_ C \_ 驗證 \_ LEVEL \_ \_** (**wbemAuthenticationLevelPktPrivacy** for script 和 Visual Basic (VB) ) authentication LEVEL。</span><span class="sxs-lookup"><span data-stu-id="46760-132">If the *Password* and *UserName* parameters are specified, the connection to WMI must use the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy** for script and Visual Basic (VB)) authentication level.</span></span>

<span data-ttu-id="46760-133">若要連接到遠端電腦並指定認證，請使用定位器物件連接（針對 c + + 為 IWbemLocator），以及針對腳本和 VB 使用 Wbemscripting.swbemlocator。</span><span class="sxs-lookup"><span data-stu-id="46760-133">To connect to a remote computer and specify credentials, use the locator object connection, which is IWbemLocator for C++, and SWbemLocator for script and VB.</span></span> <span data-ttu-id="46760-134">請勿使用「標記」連接。</span><span class="sxs-lookup"><span data-stu-id="46760-134">Do not use the moniker connection.</span></span>

<span data-ttu-id="46760-135">若要連接到本機電腦，您無法指定密碼或驗證授權單位，例如 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="46760-135">To connect to a local computer, you cannot specify a password or an authentication authority, such as Kerberos.</span></span> <span data-ttu-id="46760-136">您只能指定連接到遠端電腦的密碼和授權單位。</span><span class="sxs-lookup"><span data-stu-id="46760-136">You can only specify the password and authority in connections to remote computers.</span></span>

<span data-ttu-id="46760-137">當指定 *密碼* 和使用者 *名稱* 時，如果驗證等級太低，WMI 就會傳回針對 C/c + + **\_ \_ \_ \_ 所需的 WBEM 電子加密連接** ，以及腳本和 VB 的 **wbemErrEncryptedConnectionRequired** 。</span><span class="sxs-lookup"><span data-stu-id="46760-137">If the authentication level is too low when a *Password* and *UserName* are specified, then WMI returns the **WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED** error for C/C++, and **wbemErrEncryptedConnectionRequired** for script and VB.</span></span>

<span data-ttu-id="46760-138">如需詳細資訊，請參閱 [**Wbemscripting.swbemlocator \_ ConnectServer、**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator：： ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver)和 [建立標記字串](/windows/desktop/WmiSdk/constructing-a-moniker-string)。</span><span class="sxs-lookup"><span data-stu-id="46760-138">For more information, see [**SWbemLocator\_ConnectServer,**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator::ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver), and [Constructing a Moniker String](/windows/desktop/WmiSdk/constructing-a-moniker-string).</span></span>

## <a name="examples"></a><span data-ttu-id="46760-139">範例</span><span class="sxs-lookup"><span data-stu-id="46760-139">Examples</span></span>

<span data-ttu-id="46760-140">下列腳本說明如何重新命名本機電腦。</span><span class="sxs-lookup"><span data-stu-id="46760-140">The following script shows you how to rename a local computer.</span></span>


```VB
Name = "name"
Password = "password"
Username = "username"

Set objWMIService = GetObject("Winmgmts:root\cimv2")

' Call always gets only one Win32_ComputerSystem object.
For Each objComputer in _
    objWMIService.InstancesOf("Win32_ComputerSystem")

        Return = objComputer.rename(Name,Password,Username)
        If Return <> 0 Then
           WScript.Echo "Rename failed. Error = " & Err.Number
        Else
           WScript.Echo "Rename succeeded." & _
               " Reboot for new name to go into effect"
        End If

Next
```



<span data-ttu-id="46760-141">下列 c + + 程式碼範例會重新命名電腦系統。</span><span class="sxs-lookup"><span data-stu-id="46760-141">The following C++ code sample renames a computer system.</span></span>


```C++
int set_computer_name(const string &newname/*, const string &username, const string &password*/)
{
 HRESULT hres;


// Step 1: --------------------------------------------------
 // Initialize COM. ------------------------------------------


hres = CoInitializeEx(0, COINIT_MULTITHREADED); 
 if (FAILED(hres))
 {
 cout << "Failed to initialize COM library. Error code = 0x" 
 << hex << hres << endl;
 return 1; // Program has failed.
 }


// Step 2: --------------------------------------------------
 // Set general COM security levels --------------------------
 // Note: If you are using Windows 2000, you need to specify -
 // the default authentication credentials for a user by using
 // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
 // parameter of CoInitializeSecurity ------------------------


hres = CoInitializeSecurity(
 NULL, 
 -1, // COM authentication
 NULL, // Authentication services
 NULL, // Reserved
 RPC_C_AUTHN_LEVEL_DEFAULT, // Default authentication 
 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation 
 NULL, // Authentication info
 EOAC_NONE, // Additional capabilities 
 NULL // Reserved
 );




 if (FAILED(hres))
 {
 cout << "Failed to initialize security. Error code = 0x" 
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
 }

 // Step 3: ---------------------------------------------------
 // Obtain the initial locator to WMI -------------------------


IWbemLocator *pLoc = NULL;


hres = CoCreateInstance(
 CLSID_WbemLocator, 
 0, 
 CLSCTX_INPROC_SERVER, 
 IID_IWbemLocator, (LPVOID *) &pLoc);

 if (FAILED(hres))
 {
 cout << "Failed to create IWbemLocator object."
 << " Err code = 0x"
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 4: -----------------------------------------------------
 // Connect to WMI through the IWbemLocator::ConnectServer method


IWbemServices *pSvc = NULL;

 // Connect to the root\cimv2 namespace with
 // the current user and obtain pointer pSvc
 // to make IWbemServices calls.
 hres = pLoc->ConnectServer(
 _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
 NULL, // User name. NULL = current user
 NULL, // User password. NULL = current
 0, // Locale. NULL indicates current
 NULL, // Security flags.
 0, // Authority (e.g. Kerberos)
 0, // Context object 
 &pSvc // pointer to IWbemServices proxy
 );

 if (FAILED(hres))
 {
 cout << "Could not connect. Error code = 0x" 
 << hex << hres << endl;
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


/*cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;*/




 // Step 5: --------------------------------------------------
 // Set security levels on the proxy -------------------------


hres = CoSetProxyBlanket(
 pSvc, // Indicates the proxy to set
 RPC_C_AUTHN_WINNT, // RPC_C_AUTHN_xxx
 RPC_C_AUTHZ_NONE, // RPC_C_AUTHZ_xxx
 NULL, // Server principal name 
 RPC_C_AUTHN_LEVEL_CALL, // RPC_C_AUTHN_LEVEL_xxx 
 RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
 NULL, // client identity
 EOAC_NONE // proxy capabilities 
 );


if (FAILED(hres))
 {
 cout << "Could not set proxy blanket. Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 6: --------------------------------------------------
 // Use the IWbemServices pointer to make requests of WMI ----


// For example, get the name of the operating system
 IEnumWbemClassObject* pEnumerator = NULL;
 hres = pSvc->ExecQuery(
 bstr_t("WQL"), 
 bstr_t("SELECT * FROM Win32_ComputerSystem"),
 WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
 NULL,
 &pEnumerator);

 if (FAILED(hres))
 {
 cout << "Query for operating system name failed."
 << " Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release();
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 7: -------------------------------------------------
 // Get the data from the query in step 6 -------------------

 IWbemClassObject *pclsObj;
 ULONG uReturn = 0;

 while (pEnumerator)
 {
 HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
 &pclsObj, &uReturn);


if(0 == uReturn)
 {
 break;
 }


// set up to call the Win32_ComputerSystem::Rename method
 BSTR MethodName = SysAllocString(L"Rename");
 BSTR ClassName = SysAllocString(L"Win32_ComputerSystem");


IWbemClassObject* pClass = NULL;
 hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);


IWbemClassObject* pInParamsDefinition = NULL;
 hres = pClass->GetMethod(MethodName, 0, 
 &pInParamsDefinition, NULL);


IWbemClassObject* pClassInstance = NULL;
 hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);


// Create the values for the in parameters
 wstring val;
 BSTR NewName;
 val.assign(newname.begin(), newname.end());
 NewName = SysAllocString(val.c_str());


VARIANT varName;
 varName.vt = VT_BSTR;
 varName.bstrVal = NewName;


// Store the value for the in parameters
 hres = pClassInstance->Put(L"Name", 0,
 &varName, 0);
 wprintf(L"Set computer name to %s\n", V_BSTR(&varName));


VARIANT var;
 CIMTYPE pType;
 LONG pFlavor;
 pclsObj->Get(L"__PATH",0,&var,&pType,&pFlavor);


// Execute Method
 IWbemClassObject* pOutParams = NULL;
 hres = pSvc->ExecMethod(var.bstrVal, MethodName, 0,
 NULL, pClassInstance, &pOutParams, NULL);


if (FAILED(hres))
 {
 cout << "Could not execute method. Error code = 0x" 
 << hex << hres << endl;
 VariantClear(&varName);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 1; // Program has failed.
 }


// To see what the method returned,
 // use the following code. The return value will
 // be in &varReturnValue
 VARIANT varReturnValue;
 hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
 &varReturnValue, NULL, 0);




 // Clean up
 //--------------------------
 VariantClear(&varName);
 VariantClear(&varReturnValue);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 0;


}


// Cleanup
 // ========

 pSvc->Release();
 pLoc->Release();
 pEnumerator->Release();
 pclsObj->Release();
 CoUninitialize();


return 0; // Program successfully completed.
```



## <a name="requirements"></a><span data-ttu-id="46760-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="46760-142">Requirements</span></span>



| <span data-ttu-id="46760-143">需求</span><span class="sxs-lookup"><span data-stu-id="46760-143">Requirement</span></span> | <span data-ttu-id="46760-144">值</span><span class="sxs-lookup"><span data-stu-id="46760-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46760-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46760-145">Minimum supported client</span></span><br/> | <span data-ttu-id="46760-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46760-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46760-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46760-147">Minimum supported server</span></span><br/> | <span data-ttu-id="46760-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46760-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46760-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="46760-149">Namespace</span></span><br/>                | <span data-ttu-id="46760-150">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46760-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46760-151">MOF</span><span class="sxs-lookup"><span data-stu-id="46760-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46760-152"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="46760-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46760-153">DLL</span><span class="sxs-lookup"><span data-stu-id="46760-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46760-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46760-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46760-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46760-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46760-156">**Win32 \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="46760-156">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="46760-157">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="46760-157">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> </dl>

 

