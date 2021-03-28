---
description: 本主題說明如何為您的應用程式建立快捷方式、將 AppUserModelID 指派給該應用程式，並將它安裝在開始畫面中。
title: 如何透過 AppUserModelID 啟用桌面快顯通知
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: bd02a0ec6512aa7637f0d6b2b281e1b862e61d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972800"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a><span data-ttu-id="7a580-103">如何透過 AppUserModelID 啟用桌面快顯通知</span><span class="sxs-lookup"><span data-stu-id="7a580-103">How to enable desktop toast notifications through an AppUserModelID</span></span>

<span data-ttu-id="7a580-104">本主題說明如何為您的應用程式建立快捷方式、將 [AppUserModelID](appids.md)指派給該應用程式，並將它安裝在開始畫面中。</span><span class="sxs-lookup"><span data-stu-id="7a580-104">This topic shows you how to create a shortcut for your app, assign it an [AppUserModelID](appids.md), and install it in the Start screen.</span></span> <span data-ttu-id="7a580-105">強烈建議您在 Windows Installer 而不是在應用程式的程式碼中進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="7a580-105">We strongly recommend that you do this in the Windows Installer rather than in your app's code.</span></span> <span data-ttu-id="7a580-106">若開始畫面或 **所有程式** 中都未安裝有效的快捷方式，您就無法從桌面應用程式引發快顯通知。</span><span class="sxs-lookup"><span data-stu-id="7a580-106">Without a valid shortcut installed in the Start screen or in **All Programs**, you cannot raise a toast notification from a desktop app.</span></span>

> [!Note]  
> <span data-ttu-id="7a580-107">本主題中使用的範例方法取自桌面快顯通知 [範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)。</span><span class="sxs-lookup"><span data-stu-id="7a580-107">The example methods used in this topic are taken from the [Desktop toast sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="7a580-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="7a580-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7a580-109">技術</span><span class="sxs-lookup"><span data-stu-id="7a580-109">Technologies</span></span>

-   <span data-ttu-id="7a580-110">COM</span><span class="sxs-lookup"><span data-stu-id="7a580-110">COM</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7a580-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="7a580-111">Prerequisites</span></span>

-   <span data-ttu-id="7a580-112">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a580-112">Libraries</span></span>
    -   <span data-ttu-id="7a580-113">C + +：執行時間 .lib</span><span class="sxs-lookup"><span data-stu-id="7a580-113">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="7a580-114">C \# ： Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="7a580-114">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="7a580-115">C \# ：適用于 Microsoft .NET Framework 的 WINDOWS API 程式碼套件</span><span class="sxs-lookup"><span data-stu-id="7a580-115">C\#: Windows API Code Pack for Microsoft .NET Framework</span></span>
-   <span data-ttu-id="7a580-116">至少支援 Windows 8 的 Microsoft Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="7a580-116">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="7a580-117">指示</span><span class="sxs-lookup"><span data-stu-id="7a580-117">Instructions</span></span>

### <a name="step-1-prepare-the-shortcut-to-be-created"></a><span data-ttu-id="7a580-118">步驟1：準備要建立的快捷方式</span><span class="sxs-lookup"><span data-stu-id="7a580-118">Step 1: Prepare the shortcut to be created</span></span>

<span data-ttu-id="7a580-119">此範例會先透過 [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) 函式來決定使用者的應用程式資料檔案夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="7a580-119">This example first determines the path of the user's app data folder through the [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) function.</span></span> <span data-ttu-id="7a580-120">接著，它會撰寫快捷方式的完整路徑，判斷該名稱的快捷方式尚未存在於該位置，並將該資訊傳遞至另一個方法，以建立並安裝快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7a580-120">It then composes the full path to the shortcut, determines that a shortcut of that name does not already exist at that location, and passes that information to another method which creates and installs the shortcut.</span></span>

<span data-ttu-id="7a580-121">請注意，您可以針對每個使用者或每個應用程式部署快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7a580-121">Note that the shortcut can be deployed per-user or per-app.</span></span>


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a><span data-ttu-id="7a580-122">步驟2：建立快捷方式，並將其安裝在開始畫面</span><span class="sxs-lookup"><span data-stu-id="7a580-122">Step 2: Create the shortcut and install it in the Start screen</span></span>

<span data-ttu-id="7a580-123">這個範例也會抓取快速鍵的屬性存放區，並從先前定義的變數中設定必要的 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性 `AppID` 。</span><span class="sxs-lookup"><span data-stu-id="7a580-123">This example also retrieves the shortcut's property store and sets the required [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property from a previously defined variable, `AppID`.</span></span>


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="7a580-124">備註</span><span class="sxs-lookup"><span data-stu-id="7a580-124">Remarks</span></span>

<span data-ttu-id="7a580-125">除了本主題所示的方法之外，您還可以使用架構（例如 Windows Installer XML (WiX) ）來產生快捷方式，並將其部署為 Windows Installer 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7a580-125">As an alternative to the approach shown in this topic, you can use a framework such as the Windows Installer XML (WiX) to generate the shortcut and deploy it as part of the Windows Installer.</span></span> <span data-ttu-id="7a580-126">在此情況下，此程式碼應該包含在 MSI 中，而不是應用程式的程式碼中。</span><span class="sxs-lookup"><span data-stu-id="7a580-126">In that case, this code should be included in the MSI rather than in the app's code.</span></span> <span data-ttu-id="7a580-127">如需詳細資訊，請參閱「 [從桌面應用程式](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) 傳送快顯通知」範例中隨附的範例 WiX 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7a580-127">For more information, see the sample WiX configuration file included with the [Sending toast notifications from desktop apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a580-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a580-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a580-129">快速入門：從桌面傳送快顯通知</span><span class="sxs-lookup"><span data-stu-id="7a580-129">Quickstart: Sending a toast notification from the desktop</span></span>](quickstart-sending-desktop-toast.md)
</dt> <dt>

<span data-ttu-id="7a580-130">[從桌面應用程式範例傳送快顯通知](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="7a580-130">[Sending toast notifications from desktop apps sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span></span>
</dt> <dt>

[<span data-ttu-id="7a580-131">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="7a580-131">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> <dt>

<span data-ttu-id="7a580-132">[如何：安裝 Windows Installer XML (WiX) 工具](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-132">[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7a580-133">快顯通知 XML 架構</span><span class="sxs-lookup"><span data-stu-id="7a580-133">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="7a580-134">[快顯通知總覽](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-134">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7a580-135">[快速入門：傳送快顯通知](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-135">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7a580-136">[快速入門：傳送快顯推播通知](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-136">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7a580-137">快顯通知的指導方針和檢查清單</span><span class="sxs-lookup"><span data-stu-id="7a580-137">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[<span data-ttu-id="7a580-138">如何將影像新增至快顯通知範本</span><span class="sxs-lookup"><span data-stu-id="7a580-138">How to add images to a toast template</span></span>](/previous-versions/windows/)
</dt> <dt>

[<span data-ttu-id="7a580-139">如何檢查快顯通知設定</span><span class="sxs-lookup"><span data-stu-id="7a580-139">How to check toast notification settings</span></span>](/previous-versions/windows/)
</dt> <dt>

<span data-ttu-id="7a580-140">[如何選擇和使用快顯通知範本](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-140">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7a580-141">[如何從快顯通知處理啟用](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-141">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7a580-142">[如何加入宣告快顯通知](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-142">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7a580-143">[選擇快顯通知範本](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-143">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7a580-144">[快顯音訊選項](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a580-144">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
