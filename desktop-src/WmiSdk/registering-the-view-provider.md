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
# <a name="registering-the-view-provider"></a><span data-ttu-id="27792-104">註冊 View 提供者</span><span class="sxs-lookup"><span data-stu-id="27792-104">Registering the View Provider</span></span>

<span data-ttu-id="27792-105">WMI 安裝過程中，WMI 會自動註冊 View Provider DLL。</span><span class="sxs-lookup"><span data-stu-id="27792-105">WMI automatically registers the View Provider DLL during the WMI installation process.</span></span> <span data-ttu-id="27792-106">不過，您仍然需要針對每個將包含視圖類別的命名空間，向 WMI 註冊 View Provider。</span><span class="sxs-lookup"><span data-stu-id="27792-106">However, you still need to register the View Provider with WMI for each namespace that will contain view classes.</span></span>

<span data-ttu-id="27792-107">下列程式說明如何註冊 View Provider。</span><span class="sxs-lookup"><span data-stu-id="27792-107">The following procedure describes how to register the View Provider.</span></span>

<span data-ttu-id="27792-108">**註冊 View Provider**</span><span class="sxs-lookup"><span data-stu-id="27792-108">**To register the View Provider**</span></span>

1.  <span data-ttu-id="27792-109">建立 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例，以描述視圖提供者的執行。</span><span class="sxs-lookup"><span data-stu-id="27792-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the View Provider.</span></span>

    <span data-ttu-id="27792-110">[**\_ \_ Win32Provider**](--win32provider.md)實例描述提供者的名稱和其類別識別碼 (CLSID) 以及預設安全性設定。</span><span class="sxs-lookup"><span data-stu-id="27792-110">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (CLSID), as well as the default security settings.</span></span>

    <span data-ttu-id="27792-111">下列程式碼範例說明 [**\_ \_ Win32Provider**](--win32provider.md)的執行。</span><span class="sxs-lookup"><span data-stu-id="27792-111">The following code example describes an implementation of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  <span data-ttu-id="27792-112">建立 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="27792-112">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

    <span data-ttu-id="27792-113">下列程式碼範例顯示如何建立 **\_ \_ InstanceProviderRegistration** 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="27792-113">The following code example shows how to create an instance of the **\_\_InstanceProviderRegistration** class.</span></span>

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

3.  <span data-ttu-id="27792-114">如果您想要讓 union view 類別支援方法，請建立 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="27792-114">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class if you want to have your union view class support methods.</span></span>

    <span data-ttu-id="27792-115">下列程式碼範例顯示如何建立 **\_ \_ MethodProviderRegistration** 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="27792-115">The following code example shows how to create an instance of the **\_\_MethodProviderRegistration** class.</span></span>

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  <span data-ttu-id="27792-116">使用 MOF 編譯器 ([mofcomp.exe](mofcomp.md)) 或 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面編譯您的 mof 程式碼。</span><span class="sxs-lookup"><span data-stu-id="27792-116">Compile your MOF code using the MOF compiler ([mofcomp](mofcomp.md)) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="27792-117">如果您將先前列出的 MOF 程式碼範例儲存至名為 Viewtest 的檔案中，請使用 Mofcomp.exe 命令將 MOF 程式碼載入至目標命名空間。</span><span class="sxs-lookup"><span data-stu-id="27792-117">If you save the previously listed MOF code example into a file named Viewtest.mof, use the Mofcomp command to load the MOF code into the target namespace.</span></span> <span data-ttu-id="27792-118">*NamespacePath* 是您想要在其中建立 view 類別實例的命名空間。</span><span class="sxs-lookup"><span data-stu-id="27792-118">*NamespacePath* is the namespace in which you wish to create the view class instance.</span></span>

    <span data-ttu-id="27792-119">在命令提示字元中輸入下列命令，將 MOF 程式碼載入至目標命名空間。</span><span class="sxs-lookup"><span data-stu-id="27792-119">Type the following command at a command prompt to load the MOF code into the target namespace.</span></span>

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    <span data-ttu-id="27792-120">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="27792-120">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="27792-121">如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="27792-121">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

 

 



