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
ms.openlocfilehash: 517c2b72e830c00b105048adc63923291f896cd5d0d77569c91b1aa12e034e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459790"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>如何透過 AppUserModelID 啟用桌面快顯通知

本主題說明如何為您的應用程式建立快捷方式、將 [AppUserModelID](appids.md)指派給該應用程式，並將它安裝在開始畫面中。 強烈建議您在 Windows Installer 而不是在應用程式的程式碼中進行這項作業。 若開始畫面或 **所有程式** 中都未安裝有效的快捷方式，您就無法從桌面應用程式引發快顯通知。

> [!Note]  
> 本主題中使用的範例方法取自桌面快顯通知 [範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)。

 

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   COM

### <a name="prerequisites"></a>必要條件

-   程式庫
    -   C + +：執行時間 .lib
    -   C \# ： Windows。.Winmd
-   C \# ：適用于 Microsoft .NET Framework Windows API 程式碼套件
-   至少支援 Windows 8 的 Microsoft Visual Studio 版本

## <a name="instructions"></a>指示

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>步驟1：準備要建立的快捷方式

此範例會先透過 [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) 函式來決定使用者的應用程式資料檔案夾的路徑。 接著，它會撰寫快捷方式的完整路徑，判斷該名稱的快捷方式尚未存在於該位置，並將該資訊傳遞至另一個方法，以建立並安裝快捷方式。

請注意，您可以針對每個使用者或每個應用程式部署快捷方式。


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



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>步驟2：建立快捷方式，並將其安裝在開始畫面

這個範例也會抓取快速鍵的屬性存放區，並從先前定義的變數中設定必要的 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性 `AppID` 。


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



## <a name="remarks"></a>備註

除了本主題所示的方法之外，您還可以使用架構（例如 Windows Installer XML (WiX) ）來產生快捷方式，並將其部署為 Windows Installer 的一部分。 在此情況下，此程式碼應該包含在 MSI 中，而不是應用程式的程式碼中。 如需詳細資訊，請參閱「 [從桌面應用程式](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) 傳送快顯通知」範例中隨附的範例 WiX 設定檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門：從桌面傳送快顯通知](quickstart-sending-desktop-toast.md)
</dt> <dt>

[從桌面應用程式範例傳送快顯通知](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[應用程式使用者模型識別碼 (AppUserModelIDs) ](appids.md)
</dt> <dt>

[如何：安裝 Windows Installer XML (WiX) 工具](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[快顯通知 XML 架構](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[快顯通知總覽](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[快速入門：傳送快顯通知](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[快速入門：傳送快顯推播通知](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[快顯通知的指導方針和檢查清單](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[如何將影像新增至快顯通知範本](/previous-versions/windows/)
</dt> <dt>

[如何檢查快顯通知設定](/previous-versions/windows/)
</dt> <dt>

[如何選擇和使用快顯通知範本](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[如何從快顯通知處理啟用](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[如何加入宣告快顯通知](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[選擇快顯通知範本](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[快顯音訊選項](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
