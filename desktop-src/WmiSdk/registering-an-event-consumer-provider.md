---
description: 若要建立 WMI 事件取用者提供者，您必須 \_ \_ 使用 EventConsumerProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: 註冊事件取用者提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692200"
---
# <a name="registering-an-event-consumer-provider"></a><span data-ttu-id="8f375-103">註冊事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="8f375-103">Registering an Event Consumer Provider</span></span>

<span data-ttu-id="8f375-104">若要建立 WMI [*事件取用者提供*](gloss-e.md)者，您必須使用 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。</span><span class="sxs-lookup"><span data-stu-id="8f375-104">To create a WMI [*event consumer provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="8f375-105">如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="8f375-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="8f375-106">下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。</span><span class="sxs-lookup"><span data-stu-id="8f375-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="8f375-107">下列程式說明如何註冊事件取用者提供者。</span><span class="sxs-lookup"><span data-stu-id="8f375-107">The following procedure describes how to register an event consumer provider.</span></span>

<span data-ttu-id="8f375-108">**註冊事件取用者提供者**</span><span class="sxs-lookup"><span data-stu-id="8f375-108">**To register an event consumer provider**</span></span>

1.  <span data-ttu-id="8f375-109">建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8f375-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="8f375-110">建立 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)類別的實例，以描述提供者的功能集。</span><span class="sxs-lookup"><span data-stu-id="8f375-110">Create an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="8f375-111">[**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)所定義的屬性包含提供者的物件路徑，以及事件取用者提供者所支援之邏輯取用者類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f375-111">The properties that are defined by [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) include the object path to the provider and the names of the logical consumer classes that the event consumer provider supports.</span></span>

    <span data-ttu-id="8f375-112">請務必使用 **動態** 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號來標記類別。</span><span class="sxs-lookup"><span data-stu-id="8f375-112">Be sure to tag the class with both the **Dynamic** and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="8f375-113">**動態** 限定詞表示 WMI 應該使用提供者來取出類別實例。</span><span class="sxs-lookup"><span data-stu-id="8f375-113">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="8f375-114">**提供者** 辨識符號會指定 WMI 應使用的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="8f375-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="8f375-115">下列程式碼範例顯示如何註冊事件取用者提供者。</span><span class="sxs-lookup"><span data-stu-id="8f375-115">The following code example shows how to register an event consumer provider.</span></span>

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



