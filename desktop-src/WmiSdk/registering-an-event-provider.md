---
description: 若要建立 WMI 事件提供者，您必須 \_ \_ 使用 EventProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: 註冊事件提供者
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115801"
---
# <a name="registering-an-event-provider"></a><span data-ttu-id="f5eed-103">註冊事件提供者</span><span class="sxs-lookup"><span data-stu-id="f5eed-103">Registering an Event Provider</span></span>

<span data-ttu-id="f5eed-104">若要建立 WMI [*事件提供者*](gloss-e.md)，您必須使用 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。</span><span class="sxs-lookup"><span data-stu-id="f5eed-104">To create a WMI [*event provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventProviderRegistration**](--eventproviderregistration.md).</span></span> <span data-ttu-id="f5eed-105">如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="f5eed-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="f5eed-106">下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。</span><span class="sxs-lookup"><span data-stu-id="f5eed-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="f5eed-107">下列程式說明如何註冊事件提供者。</span><span class="sxs-lookup"><span data-stu-id="f5eed-107">The following procedure describes how to register an event provider.</span></span>

<span data-ttu-id="f5eed-108">**註冊事件提供者**</span><span class="sxs-lookup"><span data-stu-id="f5eed-108">**To register an event provider**</span></span>

1.  <span data-ttu-id="f5eed-109">建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f5eed-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="f5eed-110">建立 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別的實例，以描述提供者的功能集。</span><span class="sxs-lookup"><span data-stu-id="f5eed-110">Create an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="f5eed-111">[**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別會繼承 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)父類別的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="f5eed-111">The [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class.</span></span> <span data-ttu-id="f5eed-112">**\_ \_ EventProviderRegistration** 類別的本機屬性是提供者的物件路徑，以及描述提供者支援之事件的查詢清單。</span><span class="sxs-lookup"><span data-stu-id="f5eed-112">The properties local to the **\_\_EventProviderRegistration** class are the object path to the provider and a list of queries that describe the events that the provider supports.</span></span> <span data-ttu-id="f5eed-113">如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="f5eed-113">For more information, see [Querying WMI](querying-wmi.md).</span></span>

3.  <span data-ttu-id="f5eed-114">將 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別的執行載入至 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="f5eed-114">Load your implementation of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) classes into the WMI repository.</span></span>

    <span data-ttu-id="f5eed-115">WMI 會使用您的類別定義來註冊及存取事件提供者。</span><span class="sxs-lookup"><span data-stu-id="f5eed-115">WMI uses your class definition to register and access your event provider.</span></span> <span data-ttu-id="f5eed-116">如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f5eed-116">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="f5eed-117">下列程式碼範例說明 [**\_ \_ Win32Provider**](--win32provider.md)類別和 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別的實作為。</span><span class="sxs-lookup"><span data-stu-id="f5eed-117">The following code example describes an implementation of a [**\_\_Win32Provider**](--win32provider.md) class and a [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

<span data-ttu-id="f5eed-118">第一個查詢表示提供者會為外來事件類別 FaxEvent 產生所有事件通知。</span><span class="sxs-lookup"><span data-stu-id="f5eed-118">The first query indicates that the provider generates all event notifications for the extrinsic event class FaxEvent.</span></span> <span data-ttu-id="f5eed-119">因為它使用 ISA 運算子，第二個查詢表示提供者會針對 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別及其所有子類別的所有實例建立事件產生通知。</span><span class="sxs-lookup"><span data-stu-id="f5eed-119">Because it uses the ISA operator, the second query implies that the provider generates notifications for all instance creation events for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and all of its subclasses.</span></span>

<span data-ttu-id="f5eed-120">當提供者註冊以提供內建事件時，事件必須套用至類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="f5eed-120">When a provider registers to provide an intrinsic event, the event must apply to all instances of a class.</span></span> <span data-ttu-id="f5eed-121">換句話說，您無法寫入查詢，只針對屬於 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的部分磁片磁碟機提供實例建立事件。</span><span class="sxs-lookup"><span data-stu-id="f5eed-121">In other words, a query cannot be written to provide instance creation events for only some of the disk drives that belong to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

 

 
