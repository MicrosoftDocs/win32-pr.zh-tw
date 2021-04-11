---
description: 若要建立 WMI 方法提供者，您必須 \_ \_ 使用 MethodProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: 註冊方法提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193635"
---
# <a name="registering-a-method-provider"></a><span data-ttu-id="3042e-103">註冊方法提供者</span><span class="sxs-lookup"><span data-stu-id="3042e-103">Registering a Method Provider</span></span>

<span data-ttu-id="3042e-104">若要建立 WMI [*方法提供者*](gloss-m.md)，您必須使用 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。</span><span class="sxs-lookup"><span data-stu-id="3042e-104">To create a WMI [*method provider*](gloss-m.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_MethodProviderRegistration**](--methodproviderregistration.md).</span></span> <span data-ttu-id="3042e-105">建立 [**\_ \_ Win32Provider**](--win32provider.md)的實例之後，您必須向 WMI 註冊該提供者。</span><span class="sxs-lookup"><span data-stu-id="3042e-105">After creating an instance of [**\_\_Win32Provider**](--win32provider.md), you must register that provider with WMI.</span></span> <span data-ttu-id="3042e-106">如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。</span><span class="sxs-lookup"><span data-stu-id="3042e-106">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="3042e-107">下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。</span><span class="sxs-lookup"><span data-stu-id="3042e-107">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="3042e-108">下列程式說明如何註冊方法提供者。</span><span class="sxs-lookup"><span data-stu-id="3042e-108">The following procedure describes how to register a method provider.</span></span>

<span data-ttu-id="3042e-109">**註冊方法提供者**</span><span class="sxs-lookup"><span data-stu-id="3042e-109">**To register a method provider**</span></span>

1.  <span data-ttu-id="3042e-110">建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3042e-110">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>

    <span data-ttu-id="3042e-111">[**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)系統類別繼承 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)父類別的許多屬性，不過，與方法提供者相關的唯一屬性是 [**\_ \_ Win32Provider**](--win32provider.md)實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="3042e-111">The [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) system class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, However, the only property relevant for a method provider is the object path to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span>

2.  <span data-ttu-id="3042e-112">建立 [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)類別的實例，以描述提供者的功能集。</span><span class="sxs-lookup"><span data-stu-id="3042e-112">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="3042e-113">請務必使用 [**動態**](dynamic-qualifier.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號來標記類別。</span><span class="sxs-lookup"><span data-stu-id="3042e-113">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="3042e-114">**動態** 限定詞表示 WMI 應該使用提供者來取出類別實例。</span><span class="sxs-lookup"><span data-stu-id="3042e-114">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="3042e-115">**提供者** 辨識符號會指定 WMI 應使用的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="3042e-115">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="3042e-116">下列程式碼範例說明如何註冊方法提供者。</span><span class="sxs-lookup"><span data-stu-id="3042e-116">The following code example describes how to register a method provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



