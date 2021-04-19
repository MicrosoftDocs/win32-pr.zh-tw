---
description: WMI 安裝過程中，WMI 會自動註冊 View Provider DLL。 不過，您仍然需要針對每個將包含視圖類別的命名空間，向 WMI 註冊 View Provider。
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: 註冊 View 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980693"
---
# <a name="registering-the-view-provider"></a>註冊 View 提供者

WMI 安裝過程中，WMI 會自動註冊 View Provider DLL。 不過，您仍然需要針對每個將包含視圖類別的命名空間，向 WMI 註冊 View Provider。

下列程式說明如何註冊 View Provider。

**註冊 View Provider**

1.  建立 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例，以描述視圖提供者的執行。

    [**\_ \_ Win32Provider**](--win32provider.md)實例描述提供者的名稱和其類別識別碼 (CLSID) 以及預設安全性設定。

    下列程式碼範例說明 [**\_ \_ Win32Provider**](--win32provider.md)的執行。

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  建立 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別的實例。

    下列程式碼範例顯示如何建立 **\_ \_ InstanceProviderRegistration** 類別的實例。

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  如果您想要讓 union view 類別支援方法，請建立 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)類別的實例。

    下列程式碼範例顯示如何建立 **\_ \_ MethodProviderRegistration** 類別的實例。

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  使用 MOF 編譯器 ([mofcomp.exe](mofcomp.md)) 或 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面編譯您的 mof 程式碼。

    如果您將先前列出的 MOF 程式碼範例儲存至名為 Viewtest 的檔案中，請使用 Mofcomp.exe 命令將 MOF 程式碼載入至目標命名空間。 *NamespacePath* 是您想要在其中建立 view 類別實例的命名空間。

    在命令提示字元中輸入下列命令，將 MOF 程式碼載入至目標命名空間。

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。

 

 



