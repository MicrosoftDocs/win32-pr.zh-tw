---
title: 開發人員物件與範例程式碼
description: 本主題說明為其設計反惡意程式碼掃描介面的開發人員群組。
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 4ac11c75d5714d0706bed28264f9fa1bf03432af82107826178007e2c42243c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579908"
---
# <a name="developer-audience-and-sample-code"></a>開發人員物件與範例程式碼

反惡意程式碼掃描介面是設計來供兩組開發人員使用。

- 想要在應用程式內對反惡意程式碼產品提出要求的應用程式開發人員。
- 想要其產品為應用程式提供最佳功能之反惡意程式碼產品的協力廠商作者。

## <a name="application-developers"></a>應用程式開發人員

AMSI 是特別設計來對抗「無檔案惡意程式碼」。 能以最佳方式運用 AMSI 技術的應用程式類型包括腳本引擎、需要在使用記憶體緩衝區時進行掃描的應用程式，以及處理可包含非 PE 可執行程式碼之檔案 (例如 Microsoft Word 和 Excel 宏或 PDF 檔) 的應用程式。 不過，AMSI 技術的實用性不限於這些範例。

有兩種方式可讓您在應用程式中使用 AMSI 進行介面。

- 使用 AMSI Win32 Api。 請參閱 [反惡意程式碼掃描介面 (AMSI) 函數](/windows/desktop/amsi/antimalware-scan-interface-functions)。
- 使用 AMSI COM 介面。 請參閱 [ **IAmsiStream** 介面](/windows/desktop/api/amsi/nn-amsi-iamsistream)。

如需示範如何在您的 COM 應用程式中使用 AMSI 的範例程式碼，請參閱 [IAmsiStream 介面範例應用程式](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream)。

## <a name="third-party-creators-of-antimalware-products"></a>反惡意程式碼產品的協力廠商建立者

作為反惡意程式碼產品的建立者，您可以選擇撰寫並註冊自己的同進程 COM 伺服器， (DLL) 做為 AMSI 提供者。 該 AMSI 提供者必須執行 [ **IAntimalwareProvider** 介面](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)，且必須在同進程中執行。

請注意，在 Windows 10 之後，版本 1709 (秋季2017者的更新) ，如果您的 AMSI 提供者 DLL 相依于其路徑中的其他 dll 同時載入，則可能無法運作。 為了避免 DLL 劫持，我們建議您的提供者 DLL 將其相依性明確地 (使用安全 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) 呼叫或對等的完整路徑) 。 我們建議您不要依賴 **LoadLibrary** 搜尋行為。

下一節說明如何註冊 AMSI 提供者。 如需示範如何撰寫您自己的 AMSI 提供者 DLL 的完整程式碼範例，請參閱 [IAntimalwareProvider 介面範例應用程式](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider)。

### <a name="register-your-provider-dll-with-amsi"></a>使用 AMSI 註冊您的提供者 DLL

首先，您必須確定這些 Windows 登錄機碼存在。

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

AMSI 提供者是同進程的 COM 伺服器。 因此，它必須向 COM 註冊本身。 COM 類別是在中註冊 `HKLM\SOFTWARE\Classes\CLSID` 。

下列程式碼示範如何註冊 AMSI 提供者，其 GUID (此範例) 我們將假設為 `2E5D8A62-77F9-4F7B-A90C-2744820139B2` 。

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

如果您的 DLL 實[DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)函式（如上述範例所示），則您可以使用 Windows 提供的可執行檔來註冊它 `regsvr32.exe` 。 從提升許可權的命令提示字元，發出此表單的命令。

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

在此範例中，此命令會建立下列專案。

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**(預設) REG_SZ AMSI 提供者實作為範例**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**(預設) REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**>threadingmodel REG_SZ 兩者**

除了一般的 COM 註冊之外，您還需要向 AMSI 註冊提供者。 做法是將專案加入至下列索引鍵。

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

例如

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
