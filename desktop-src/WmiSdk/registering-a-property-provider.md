---
description: 若要建立 WMI 屬性提供者，您必須 \_ \_ 使用 PropertyProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: 註冊屬性提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192085"
---
# <a name="registering-a-property-provider"></a><span data-ttu-id="352bf-103">註冊屬性提供者</span><span class="sxs-lookup"><span data-stu-id="352bf-103">Registering a Property Provider</span></span>

<span data-ttu-id="352bf-104">若要建立 WMI [*屬性提供者*](gloss-p.md)，您必須使用 [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。</span><span class="sxs-lookup"><span data-stu-id="352bf-104">To create a WMI [*property provider*](gloss-p.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span> <span data-ttu-id="352bf-105">如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="352bf-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="352bf-106">下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。</span><span class="sxs-lookup"><span data-stu-id="352bf-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="352bf-107">下列程式說明如何註冊屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="352bf-107">The following procedure describes how to register a property provider.</span></span>

<span data-ttu-id="352bf-108">**註冊屬性提供者**</span><span class="sxs-lookup"><span data-stu-id="352bf-108">**To register a property provider**</span></span>

1.  <span data-ttu-id="352bf-109">建立描述屬性提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="352bf-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the property provider.</span></span>

    <span data-ttu-id="352bf-110">[**\_ \_ Win32Provider**](--win32provider.md)類別接受其他屬性的預設值，例如 **單純** 屬性的 **TRUE** 值。</span><span class="sxs-lookup"><span data-stu-id="352bf-110">The [**\_\_Win32Provider**](--win32provider.md) class accepts the default values for other properties, such as the **TRUE** value for the **Pure** property.</span></span> <span data-ttu-id="352bf-111">如需詳細資訊，請參閱 [**\_ \_ Win32Provider**](--win32provider.md)。</span><span class="sxs-lookup"><span data-stu-id="352bf-111">For more information, see [**\_\_Win32Provider**](--win32provider.md).</span></span>

2.  <span data-ttu-id="352bf-112">建立 [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md)類別的實例，以描述提供者的功能集。</span><span class="sxs-lookup"><span data-stu-id="352bf-112">Create an instance of the [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="352bf-113">[**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md)類別會繼承 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)父類別的許多屬性，其提供布林值，指出支援特定功能和字串陣列以表示查詢支援。</span><span class="sxs-lookup"><span data-stu-id="352bf-113">The [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="352bf-114">請務必使用 [**動態**](dynamic-qualifier.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號來標記類別。</span><span class="sxs-lookup"><span data-stu-id="352bf-114">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="352bf-115">**動態** 限定詞表示 WMI 應該使用動態提供者來抓取包含支援屬性的類別實例。</span><span class="sxs-lookup"><span data-stu-id="352bf-115">The **Dynamic** qualifier signals that WMI should use a dynamic provider to retrieve the class instances that contain the supported properties.</span></span> <span data-ttu-id="352bf-116">**提供者** 辨識符號會指定 WMI 應使用的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="352bf-116">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="352bf-117">當用戶端取用者註冊的事件篩選器查詢包含該事件提供者所支援之事件的參考時，WMI 會呼叫事件提供者上的 NewQuery。</span><span class="sxs-lookup"><span data-stu-id="352bf-117">WMI calls NewQuery on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="352bf-118">因此，負責 EmailClass 類別之實例修改事件的事件提供者可以設定為只針對寄件者產生通知。</span><span class="sxs-lookup"><span data-stu-id="352bf-118">So the event provider responsible for instance modification events for the EmailClass class can be set up to generate notifications only for sender.</span></span> <span data-ttu-id="352bf-119">當提供者收到要求主體屬性變更通知的查詢時，提供者可以開始產生這些通知。</span><span class="sxs-lookup"><span data-stu-id="352bf-119">When the provider receives a query requesting notification of changes to the subject property, the provider can start generating those notifications.</span></span> <span data-ttu-id="352bf-120">在此案例中，您不需要 WMI 來捨棄報告收件者變更的通知。</span><span class="sxs-lookup"><span data-stu-id="352bf-120">In this scenario, WMI is not required to discard the notifications that report recipient changes only.</span></span>

<span data-ttu-id="352bf-121">下列 MOF 程式碼範例說明可以用來註冊屬性提供者的實例。</span><span class="sxs-lookup"><span data-stu-id="352bf-121">The following MOF code example describes instances that can be used to register a property provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> <span data-ttu-id="352bf-122">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md)的實例，來註冊或刪除屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="352bf-122">Only administrators can register or delete a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span>

 

 

 



