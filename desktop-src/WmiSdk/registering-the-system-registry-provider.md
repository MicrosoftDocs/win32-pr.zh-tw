---
description: System Registry 提供者會在 Windows 上註冊為 WMI 安裝程式的一部分。
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: 註冊系統登錄提供者
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977241"
---
# <a name="registering-the-system-registry-provider"></a><span data-ttu-id="eaf88-103">註冊系統登錄提供者</span><span class="sxs-lookup"><span data-stu-id="eaf88-103">Registering the System Registry Provider</span></span>

<span data-ttu-id="eaf88-104">System Registry 提供者會在 Windows 上註冊為 WMI 安裝程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="eaf88-104">The System Registry provider is registered as part of the WMI installation process on Windows.</span></span> <span data-ttu-id="eaf88-105">如果您使用的是其他平臺，而且想要使用系統登錄提供者，您必須先依照下列步驟來註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="eaf88-105">If you are using another platform and want to use the System Registry provider, you must first register the provider yourself following the steps described below.</span></span>

<span data-ttu-id="eaf88-106">下列程式說明如何註冊系統登錄提供者。</span><span class="sxs-lookup"><span data-stu-id="eaf88-106">The following procedure describes how to register the System Registry provider.</span></span>

<span data-ttu-id="eaf88-107">**註冊系統登錄提供者**</span><span class="sxs-lookup"><span data-stu-id="eaf88-107">**To register the System Registry provider**</span></span>

1.  <span data-ttu-id="eaf88-108">將提供者註冊為 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eaf88-108">Register the provider as a COM server.</span></span>

    <span data-ttu-id="eaf88-109">如有必要，您可能需要建立登錄專案。</span><span class="sxs-lookup"><span data-stu-id="eaf88-109">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="eaf88-110">此程式適用于所有的 COM 伺服器，而且與 WMI 無關。</span><span class="sxs-lookup"><span data-stu-id="eaf88-110">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="eaf88-111">如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的 [COM](https://msdn.microsoft.com/library/aa139695.aspx) 檔。</span><span class="sxs-lookup"><span data-stu-id="eaf88-111">For more information, see the [COM](https://msdn.microsoft.com/library/aa139695.aspx) documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

2.  <span data-ttu-id="eaf88-112">建立 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例，以描述系統登錄提供者的執行。</span><span class="sxs-lookup"><span data-stu-id="eaf88-112">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the System Registry provider.</span></span>

    <span data-ttu-id="eaf88-113">[**\_ \_ Win32Provider**](--win32provider.md)實例描述提供者的名稱及其類別識別碼 (**CLSID**) 。</span><span class="sxs-lookup"><span data-stu-id="eaf88-113">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (**CLSID**).</span></span>

    <span data-ttu-id="eaf88-114">下列範例說明如何將 [**\_ \_ Win32Provider**](--win32provider.md)註冊為實例屬性、事件或方法提供者。</span><span class="sxs-lookup"><span data-stu-id="eaf88-114">The following example describes how to register [**\_\_Win32Provider**](--win32provider.md) as an instance property, event, or method provider.</span></span>

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  <span data-ttu-id="eaf88-115">建立衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)類別的一或多個類別實例，以描述系統登錄提供者的邏輯實作為。</span><span class="sxs-lookup"><span data-stu-id="eaf88-115">Create one or more instances of classes derived from the [**\_\_ProviderRegistration**](--providerregistration.md) class to describe the logical implementation of the System Registry provider.</span></span>

    <span data-ttu-id="eaf88-116">根據您註冊系統登錄提供者的目的，您可以建立下列一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="eaf88-116">Depending on the purpose for which you are registering the System Registry provider, you can create one or more of the following classes.</span></span>

    [<span data-ttu-id="eaf88-117">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="eaf88-117">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

    [<span data-ttu-id="eaf88-118">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="eaf88-118">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

    [<span data-ttu-id="eaf88-119">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="eaf88-119">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

    [<span data-ttu-id="eaf88-120">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="eaf88-120">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

    <span data-ttu-id="eaf88-121">下列 MOF 程式碼範例說明如何以實例、屬性、事件或方法提供者的形式註冊 System Registry provider。</span><span class="sxs-lookup"><span data-stu-id="eaf88-121">The following MOF code example describes how you can register the System Registry provider as an instance, property, event, or method provider.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  <span data-ttu-id="eaf88-122">使用 MOF 編譯器或 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="eaf88-122">Compile the MOF file using the MOF compiler or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

<span data-ttu-id="eaf88-123">Windows SDK 的 WMI 區段中所提供的 RegEvent mof 檔案包含將 System Registry 提供者註冊為事件提供者所需的 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)實例。</span><span class="sxs-lookup"><span data-stu-id="eaf88-123">The RegEvent.mof file provided in the WMI section of the Windows SDK contains the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) instances necessary to register the System Registry provider as an event provider.</span></span> <span data-ttu-id="eaf88-124">如需註冊提供者的詳細資訊，請參閱 [註冊提供者](registering-a-provider.md) 和 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="eaf88-124">For more information about registering a provider, see [Registering a Provider](registering-a-provider.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 



