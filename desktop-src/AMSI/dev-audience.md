---
title: 開發人員物件與範例程式碼
description: 本主題說明為其設計反惡意程式碼掃描介面的開發人員群組。
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: 272ba17a215d0d27bb7918fee1192d4954ccc576
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2020
ms.locfileid: "104022965"
---
# <a name="developer-audience-and-sample-code"></a><span data-ttu-id="558d9-103">開發人員物件與範例程式碼</span><span class="sxs-lookup"><span data-stu-id="558d9-103">Developer audience, and sample code</span></span>

<span data-ttu-id="558d9-104">反惡意程式碼掃描介面是設計來供兩組開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="558d9-104">The Antimalware Scan Interface is designed for use by two groups of developers.</span></span>

- <span data-ttu-id="558d9-105">想要在應用程式內對反惡意程式碼產品提出要求的應用程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="558d9-105">Application developers who want to make requests to antimalware products from within their apps.</span></span>
- <span data-ttu-id="558d9-106">想要其產品為應用程式提供最佳功能之反惡意程式碼產品的協力廠商作者。</span><span class="sxs-lookup"><span data-stu-id="558d9-106">Third-party creators of antimalware products who want their products to offer the best features to applications.</span></span>

## <a name="application-developers"></a><span data-ttu-id="558d9-107">應用程式開發人員</span><span class="sxs-lookup"><span data-stu-id="558d9-107">Application developers</span></span>

<span data-ttu-id="558d9-108">AMSI 是特別設計來對抗「無檔案惡意程式碼」。</span><span class="sxs-lookup"><span data-stu-id="558d9-108">AMSI is designed in particular to combat "fileless malware".</span></span> <span data-ttu-id="558d9-109">能以最佳方式運用 AMSI 技術的應用程式類型包括腳本引擎、需要在使用記憶體緩衝區時進行掃描的應用程式，以及處理可包含非 PE 可執行程式碼之檔案 (例如 Microsoft Word 和 Excel 宏或 PDF 檔) 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="558d9-109">Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).</span></span> <span data-ttu-id="558d9-110">不過，AMSI 技術的實用性不限於這些範例。</span><span class="sxs-lookup"><span data-stu-id="558d9-110">However, the usefulness of AMSI technology is not limited to those examples.</span></span>

<span data-ttu-id="558d9-111">有兩種方式可讓您在應用程式中使用 AMSI 進行介面。</span><span class="sxs-lookup"><span data-stu-id="558d9-111">There are two ways in which you can interface with AMSI in your application.</span></span>

- <span data-ttu-id="558d9-112">使用 AMSI Win32 Api。</span><span class="sxs-lookup"><span data-stu-id="558d9-112">By using the AMSI Win32 APIs.</span></span> <span data-ttu-id="558d9-113">請參閱 [反惡意程式碼掃描介面 (AMSI) 函數](/windows/desktop/amsi/antimalware-scan-interface-functions)。</span><span class="sxs-lookup"><span data-stu-id="558d9-113">See [Antimalware Scan Interface (AMSI) functions](/windows/desktop/amsi/antimalware-scan-interface-functions).</span></span>
- <span data-ttu-id="558d9-114">使用 AMSI COM 介面。</span><span class="sxs-lookup"><span data-stu-id="558d9-114">By using the AMSI COM interfaces.</span></span> <span data-ttu-id="558d9-115">請參閱 [ **IAmsiStream** 介面](/windows/desktop/api/amsi/nn-amsi-iamsistream)。</span><span class="sxs-lookup"><span data-stu-id="558d9-115">See [**IAmsiStream** interface](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span></span>

<span data-ttu-id="558d9-116">如需示範如何在您的 COM 應用程式中使用 AMSI 的範例程式碼，請參閱 [IAmsiStream 介面範例應用程式](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream)。</span><span class="sxs-lookup"><span data-stu-id="558d9-116">For sample code showing how to consume AMSI within your COM application, see the [IAmsiStream interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span></span>

## <a name="third-party-creators-of-antimalware-products"></a><span data-ttu-id="558d9-117">反惡意程式碼產品的協力廠商建立者</span><span class="sxs-lookup"><span data-stu-id="558d9-117">Third-party creators of antimalware products</span></span>

<span data-ttu-id="558d9-118">作為反惡意程式碼產品的建立者，您可以選擇撰寫並註冊自己的同進程 COM 伺服器， (DLL) 做為 AMSI 提供者。</span><span class="sxs-lookup"><span data-stu-id="558d9-118">As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.</span></span> <span data-ttu-id="558d9-119">該 AMSI 提供者必須執行 [ **IAntimalwareProvider** 介面](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)，且必須在同進程中執行。</span><span class="sxs-lookup"><span data-stu-id="558d9-119">That AMSI provider must implement the [**IAntimalwareProvider** interface](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), and it must run in-process.</span></span>

<span data-ttu-id="558d9-120">請注意，在 Windows 10 之後，版本 1709 (秋季2017者的更新) ，如果您的 AMSI 提供者 DLL 相依于其路徑中的其他 Dll 同時載入，則可能無法運作。</span><span class="sxs-lookup"><span data-stu-id="558d9-120">Note that, after Windows 10, version 1709 (the Fall 2017 Creators' Update), your AMSI provider DLL may not work if it depends upon other DLLs in its path to be loaded at the same time.</span></span> <span data-ttu-id="558d9-121">為了避免 DLL 劫持，我們建議您的提供者 DLL 將其相依性明確地 (使用安全 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) 呼叫或對等的完整路徑) 。</span><span class="sxs-lookup"><span data-stu-id="558d9-121">To prevent DLL hijacking, we recommend that your provider DLL load its dependencies explicitly (with a full path) using secure [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) calls, or equivalent.</span></span> <span data-ttu-id="558d9-122">我們建議您不要依賴 **LoadLibrary** 搜尋行為。</span><span class="sxs-lookup"><span data-stu-id="558d9-122">We recommend this instead of relying on the **LoadLibrary** search behavior.</span></span>

<span data-ttu-id="558d9-123">下一節說明如何註冊 AMSI 提供者。</span><span class="sxs-lookup"><span data-stu-id="558d9-123">The section below shows how to register your AMSI provider.</span></span> <span data-ttu-id="558d9-124">如需示範如何撰寫您自己的 AMSI 提供者 DLL 的完整程式碼範例，請參閱 [IAntimalwareProvider 介面範例應用程式](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider)。</span><span class="sxs-lookup"><span data-stu-id="558d9-124">For full sample code showing how to author your own AMSI provider DLL, see the [IAntimalwareProvider interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span></span>

### <a name="register-your-provider-dll-with-amsi"></a><span data-ttu-id="558d9-125">使用 AMSI 註冊您的提供者 DLL</span><span class="sxs-lookup"><span data-stu-id="558d9-125">Register your provider DLL with AMSI</span></span>

<span data-ttu-id="558d9-126">首先，您必須確定這些 Windows 登錄機碼存在。</span><span class="sxs-lookup"><span data-stu-id="558d9-126">To begin with, you need to ensure that these Windows Registry keys exist.</span></span>

- <span data-ttu-id="558d9-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span><span class="sxs-lookup"><span data-stu-id="558d9-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span></span>
- <span data-ttu-id="558d9-128">HKLM\SOFTWARE\Classes\CLSID</span><span class="sxs-lookup"><span data-stu-id="558d9-128">HKLM\SOFTWARE\Classes\CLSID</span></span>

<span data-ttu-id="558d9-129">AMSI 提供者是同進程的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="558d9-129">An AMSI provider is an in-process COM server.</span></span> <span data-ttu-id="558d9-130">因此，它必須向 COM 註冊本身。</span><span class="sxs-lookup"><span data-stu-id="558d9-130">Consequently, it needs to register itself with COM.</span></span> <span data-ttu-id="558d9-131">COM 類別是在中註冊 `HKLM\SOFTWARE\Classes\CLSID` 。</span><span class="sxs-lookup"><span data-stu-id="558d9-131">COM classes are registered in `HKLM\SOFTWARE\Classes\CLSID`.</span></span>

<span data-ttu-id="558d9-132">下列程式碼示範如何註冊 AMSI 提供者，其 GUID (此範例) 我們將假設為 `2E5D8A62-77F9-4F7B-A90C-2744820139B2` 。</span><span class="sxs-lookup"><span data-stu-id="558d9-132">The code below shows how to register an AMSI provider, whose GUID (for this example) we will assume is `2E5D8A62-77F9-4F7B-A90C-2744820139B2`.</span></span>

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

<span data-ttu-id="558d9-133">如果您的 DLL 實 [DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)函式（如上述範例所示），則您可以使用 Windows 提供的可執行檔來註冊它 `regsvr32.exe` 。</span><span class="sxs-lookup"><span data-stu-id="558d9-133">If your DLL implements the [DllRegisterServer function](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), as the example above does, then you can register it by using the Windows-supplied executable `regsvr32.exe`.</span></span> <span data-ttu-id="558d9-134">從提升許可權的命令提示字元，發出此表單的命令。</span><span class="sxs-lookup"><span data-stu-id="558d9-134">From an elevated command prompt, issue a command of this form.</span></span>

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

<span data-ttu-id="558d9-135">在此範例中，此命令會建立下列專案。</span><span class="sxs-lookup"><span data-stu-id="558d9-135">In this example, the command creates the following entries.</span></span>

<span data-ttu-id="558d9-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="558d9-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

<span data-ttu-id="558d9-137">&nbsp;&nbsp;&nbsp;&nbsp;**(預設) REG_SZ AMSI 提供者實作為範例**</span><span class="sxs-lookup"><span data-stu-id="558d9-137">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_SZ    Sample AMSI Provider implementation**</span></span>


<span data-ttu-id="558d9-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="558d9-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**</span></span>

<span data-ttu-id="558d9-139">&nbsp;&nbsp;&nbsp;&nbsp;**(預設) REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**</span><span class="sxs-lookup"><span data-stu-id="558d9-139">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_EXPAND_SZ    %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**</span></span>

<span data-ttu-id="558d9-140">&nbsp;&nbsp;&nbsp;&nbsp;**>threadingmodel REG_SZ 兩者**</span><span class="sxs-lookup"><span data-stu-id="558d9-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel    REG_SZ    Both**</span></span>

<span data-ttu-id="558d9-141">除了一般的 COM 註冊之外，您還需要向 AMSI 註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="558d9-141">In addition to regular COM registration, you also need to enroll the provider with AMSI.</span></span> <span data-ttu-id="558d9-142">做法是將專案加入至下列索引鍵。</span><span class="sxs-lookup"><span data-stu-id="558d9-142">You do that by adding an entry to the following key.</span></span>

<span data-ttu-id="558d9-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span><span class="sxs-lookup"><span data-stu-id="558d9-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span></span>

<span data-ttu-id="558d9-144">例如，</span><span class="sxs-lookup"><span data-stu-id="558d9-144">For example,</span></span>

<span data-ttu-id="558d9-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="558d9-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>
