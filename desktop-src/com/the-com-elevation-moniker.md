---
title: COM 提高許可權的標記
description: COM 提高許可權的標記可讓在 [使用者帳戶控制] 下執行的應用程式 (UAC) ，以較高的許可權啟動 COM 類別。 如需詳細資訊，請參閱將焦點放在最低許可權。
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d11980c9c6a54a06991d6f2ab189640414dc5072dd913e450ce6fe33487f747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103861"
---
# <a name="the-com-elevation-moniker"></a>COM 提高許可權的標記

COM 提高許可權的標記可讓在 [使用者帳戶控制] 下執行的應用程式 (UAC) ，以較高的許可權啟動 COM 類別。 如需詳細資訊，請參閱將 [焦點放在最低許可權](/previous-versions/dotnet/articles/aa480194(v=msdn.10))。

## <a name="when-to-use-the-elevation-moniker"></a>使用提高許可權的標記時機

提高許可權的標記是用來啟動 COM 類別，以完成需要較高許可權的特定且受限功能，例如變更系統日期和時間。

提高許可權需要同時參與 COM 類別和其用戶端。 COM 類別必須設定為支援提高許可權，方法是標注其登錄專案，如需求一節中所述。 COM 用戶端必須使用提升許可權的標記來要求提高許可權。

提高許可權的標記並非為了提供應用程式相容性。 例如，如果您想要以提升許可權的伺服器來執行舊版 COM 應用程式（例如 WinWord），則應該將 COM 用戶端可執行檔設定為需要提高許可權，而不是使用提高許可權的標記來啟動繼承應用程式的類別。 當提高許可權的 COM 用戶端使用繼承應用程式的 CLSID 呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 時，用戶端的提高許可權狀態將會流向伺服器進程。

並非所有 COM 功能都與提高許可權相容。 將無法運作的功能包括：

-   提高許可權不會從用戶端流向遠端 COM 伺服器。 如果用戶端以提高許可權的標記啟動遠端 COM 伺服器，伺服器將不會提高許可權，即使它支援提高許可權也一樣。
-   如果提升許可權的 COM 類別在 COM 呼叫期間使用模擬，它可能會在模擬期間失去其較高的許可權。
-   如果提高許可權的 COM 伺服器在執行中的物件資料表中註冊類別 (衰減) ，則該類別將無法供非提高許可權的用戶端使用。
-   使用 UAC 機制提高許可權的進程不會在 COM 啟用期間載入每個使用者類別。 針對 COM 應用程式，這表示如果應用程式是由非特殊許可權的帳戶和特殊許可權帳戶使用，則必須在 **HKEY \_ 本機 \_ 電腦** 登錄 hive 中安裝應用程式的 COM 類別。 如果特殊許可權帳戶從未使用過應用程式，則應用程式的 COM 類別只需要安裝在 **HKEY \_ USERS** hive 中。
-   不允許從非提高許可權到提升許可權的應用程式使用拖放功能。

## <a name="requirements"></a>規格需求

若要使用提升許可權的標記來啟動 COM 類別，必須將類別設定為以啟動使用者或 ' Activate as Activator ' 應用程式身分識別來執行。 如果將類別設定為在任何其他身分識別下執行，則啟用會傳回錯誤的共同 \_ E \_ RUNAS \_ 值 \_ 必須 \_ 是 \_ AAA。

類別也必須以「易記」顯示名稱標注，該名稱是多語系使用者介面 (MUI) 相容。 這需要下列登錄專案：

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

如果遺漏此專案，啟用會傳回錯誤（共 E），即 \_ \_ 遺漏 \_ DISPLAYNAME。 如果缺少 MUI 檔案，則會傳回 [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) 函式的錯誤碼。

（選擇性）若要指定 UAC 使用者介面所顯示的應用程式圖示，請新增下列登錄機碼：

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**IconReference** 會使用與 **>localizedstring** 相同的格式：

@*pathtobinary*、*-resourcenumber*

此外，COM 元件也必須經過簽署，才能顯示圖示。

COM 類別也必須標注為啟用 LUA。 這需要下列登錄專案：

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

如果遺漏此專案，則啟用會傳回 \_ \_ 已停用的共同電子提高許可權錯誤 \_ 。

請注意，這些專案必須存在於 HKEY \_ 本機 \_ 電腦 hive 中，而不是 HKEY \_ CURRENT \_ USER 或 HKEY \_ USERS hive。 這可防止使用者提高本身沒有註冊之許可權的 COM 類別。

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>提高許可權的標記和提高許可權 UI

如果用戶端已經提高許可權，使用提高許可權的標記將不會造成提高許可權的 UI 顯示。

## <a name="how-to-use-the-elevation-moniker"></a>如何使用提升許可權的標記

提高許可權的標記是標準的 COM 標記，類似于會話、資料分割或佇列的名字。 它會將啟用要求導向具有指定提高許可權層級的指定伺服器。 要啟用的 CLSID 會出現在 [標記] 字串中。

提高許可權的標記支援下列執行層級權杖：

1.  系統管理員
2.  最高

其語法如下所示：

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

上述語法使用 "new" 標記來傳回 *guid* 所指定之 COM 類別的實例。 請注意，"new" 標記會在內部使用 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面取得類別物件，然後在其上呼叫 [**IClassFactory：： CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 。

提高許可權的標記也可以用來取得 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)的類別物件。 呼叫端接著會呼叫 [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 來取得物件實例。 其語法如下所示：

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>範例程式碼

下列程式碼範例示範如何使用提升許可權的標記。 它會假設您已經在目前的執行緒上初始化 COM。


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



系結 [**\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1)是 Windows Vista 的新功能。 它衍生自 [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)。

唯一的加法是 **hwnd** 欄位 **hwnd**。 這個控制碼代表的視窗會成為提高許可權 UI 的擁有者（如果適用）。

如果 **hwnd** 為 **Null**，COM 將會呼叫 [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) 來尋找與目前線程相關聯的視窗控制碼。 如果用戶端是無法填入系結 [**\_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) 結構的腳本，就可能會發生此情況。 在此情況下，COM 將會嘗試使用與腳本執行緒相關聯的視窗。

## <a name="over-the-shoulder-ots-elevation"></a>過度 (OTS) 提高許可權

 (的 OTS) 提高許可權是指用戶端以系統管理員的認證（而非自己的認證）執行 COM 伺服器的案例。  (「超過肩」一詞表示系統管理員會在用戶端執行伺服器時，監看用戶端的肩。 ) 

這種情況可能會對伺服器造成 COM 呼叫的問題，因為伺服器可能不會明確 (地呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，也就是以程式設計方式) 或隱含 (以宣告方式使用登錄) 。 針對這類伺服器，COM 會計算安全描述項，只允許自助、系統和內建系統 \\ 管理員對伺服器進行 COM 呼叫。 在 OTS 案例中，這種相片順序將無法運作。 相反地，伺服器必須明確或隱含地呼叫 **CoInitializeSecurity**，並指定包含互動式群組 SID 和系統的 ACL。

下列程式碼範例示範如何使用互動式群組 SID (SD) 建立安全描述項。

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

下列程式碼範例示範如何使用先前程式碼範例中的 SD 來隱含呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ：


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



下列程式碼範例示範如何使用上述 SD 明確呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ：


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a>COM 許可權和強制存取標籤

WindowsVista 引進了安全描述項中 *強制存取標籤* 的概念。 標籤會指示用戶端是否可以取得 COM 物件的執行存取權。 標籤會指定在系統存取控制清單中， (SACL) 部分的安全描述項中。 在 Windows Vista 中，COM 支援「系統 \_ 強制 \_ 標籤 \_ 無執行」卷 \_ \_ 標。 在 Windows Vista 之前的作業系統上，系統會忽略 COM 許可權中的 sacl。

從 Windows Vista，dcomcnfg.exe 不支援變更 COM 許可權中 (IL) 的完整性層級。 它必須以程式設計的方式設定。

下列程式碼範例示範如何建立具有標籤的 COM 安全描述項，以允許來自所有低 IL 用戶端的啟動/啟用要求。 請注意，標籤對於啟動/啟用和呼叫許可權都有效。 因此，您可以撰寫不允許啟動、啟用或從具有特定 IL 之用戶端呼叫的 COM 伺服器。 For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a>CoCreateInstance 和完整性層級

在 Windows Vista 中， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的行為已變更，以防止較低的 IL 用戶端預設系結至 COM 伺服器。 伺服器必須藉由指定 SACL 來明確地允許這類系結。 **CoCreateInstance** 的變更如下：

1.  啟動 COM 伺服器進程時，伺服器進程 token 中的 IL 會設定為用戶端或伺服器權杖 IL，以較低者為准。
2.  根據預設，COM 會防止低 IL 用戶端系結至任何 COM 伺服器的執行中實例。 若要允許系結，COM 伺服器的啟動/啟用安全描述項必須包含指定低 IL 標籤的 SACL (請參閱上一節中的範例程式碼，以建立這類安全描述項) 。

## <a name="elevated-servers-and-rot-registrations"></a>提高許可權的伺服器和 ROT 註冊

如果 COM 伺服器希望在執行中的物件資料表中註冊 (的 ROT) 並允許任何用戶端存取註冊，則必須使用 ROTFLAGS \_ ALLOWANYCLIENT 旗標。 "Activate As Activator" COM 伺服器無法指定 ROTFLAGS \_ ALLOWANYCLIENT，因為 DCOM 服務控制管理員 (DCOMSCM) 強制對此旗標進行詐騙檢查。 因此，在 Windows Vista 中，COM 加入了新的登錄專案的支援，可讓伺服器規定其衰減註冊可供任何用戶端使用：

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

此登錄 DWORD 專案唯一有效的值 \_ 為：

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

專案必須存在於 **HKEY \_ 本機 \_ 電腦** hive 中。

此專案提供「啟用為啟動程式」伺服器，其功能與 ROTFLAGS \_ ALLOWANYCLIENT 為 RunAs 伺服器提供的功能相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> <dt>

[了解「受保護模式」Internet Explorer 並在此模式下工作](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 