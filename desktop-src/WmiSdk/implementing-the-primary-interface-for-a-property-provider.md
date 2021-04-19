---
description: 屬性提供者會使用 IWbemPropertyProvider 方法做為 WMI 的主要介面。 您可以使用 IWbemPropertyProvider 來執行程式碼，以取得和修改類別和實例屬性。
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: 執行屬性提供者的主要介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975798"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a><span data-ttu-id="611fb-104">執行屬性提供者的主要介面</span><span class="sxs-lookup"><span data-stu-id="611fb-104">Implementing the Primary Interface for a Property Provider</span></span>

<span data-ttu-id="611fb-105">屬性提供者會使用 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 方法做為 WMI 的主要介面。</span><span class="sxs-lookup"><span data-stu-id="611fb-105">A property provider uses the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods as the primary interface to WMI.</span></span> <span data-ttu-id="611fb-106">您可以使用 **IWbemPropertyProvider** 來執行程式碼，以取得和修改類別和實例屬性。</span><span class="sxs-lookup"><span data-stu-id="611fb-106">With **IWbemPropertyProvider**, you can implement the code to retrieve and modify class and instance properties.</span></span>

<span data-ttu-id="611fb-107">下表列出可為屬性提供者執行的 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 方法。</span><span class="sxs-lookup"><span data-stu-id="611fb-107">The following table lists the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods that you can implement for a property provider.</span></span>



| <span data-ttu-id="611fb-108">方法</span><span class="sxs-lookup"><span data-stu-id="611fb-108">Method</span></span>                                                   | <span data-ttu-id="611fb-109">功能</span><span class="sxs-lookup"><span data-stu-id="611fb-109">Feature</span></span>      |
|----------------------------------------------------------|--------------|
| [<span data-ttu-id="611fb-110">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="611fb-110">**GetProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | <span data-ttu-id="611fb-111">重建</span><span class="sxs-lookup"><span data-stu-id="611fb-111">Retrieval</span></span>    |
| [<span data-ttu-id="611fb-112">**PutProperty**</span><span class="sxs-lookup"><span data-stu-id="611fb-112">**PutProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | <span data-ttu-id="611fb-113">修改</span><span class="sxs-lookup"><span data-stu-id="611fb-113">Modification</span></span> |



 

> [!Note]  
> <span data-ttu-id="611fb-114">您必須將屬性提供者實作為同進程提供者。</span><span class="sxs-lookup"><span data-stu-id="611fb-114">You must implement a property provider as an in-process provider.</span></span> <span data-ttu-id="611fb-115">WMI 將會初始化以服務或可執行檔撰寫的屬性提供者，但永遠不會呼叫其 [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) 和 [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) 方法。</span><span class="sxs-lookup"><span data-stu-id="611fb-115">WMI will initialize property providers written as services or executable files but will never call their [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) methods.</span></span>

 

<span data-ttu-id="611fb-116">如果您選擇不支援其中一種方法，則您的提供者可以提供可傳回 **無法使用 WBEM \_ E \_ 提供者 \_ \_** 的存根執行。</span><span class="sxs-lookup"><span data-stu-id="611fb-116">If you choose not to support one of these methods, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span>

<span data-ttu-id="611fb-117">屬性提供者會以三個限定詞的集合來識別 managed 類別或實例： **PropertyCoNtext**、 **InstanceCoNtext** 和 **ClassCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="611fb-117">A property provider identifies a managed class or instance by a set of three qualifiers: **PropertyContext**, **InstanceContext**, and **ClassContext**.</span></span> <span data-ttu-id="611fb-118">WMI 會將描述這三個限定詞的字串常數傳遞給您的屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="611fb-118">WMI will pass in string constants describing these three qualifiers to your property provider.</span></span>

<span data-ttu-id="611fb-119">您的屬性提供者必須準備好處理下列類型的內容限定詞：</span><span class="sxs-lookup"><span data-stu-id="611fb-119">Your property provider must be prepared to handle the following types of context qualifiers:</span></span>

-   <span data-ttu-id="611fb-120">**InstanceCoNtext** 辨識符號會附加至實例，並包含適用于實例中每個屬性的資訊。</span><span class="sxs-lookup"><span data-stu-id="611fb-120">The **InstanceContext** qualifier is attached to an instance and contains information that applies to every property in the instance.</span></span>
-   <span data-ttu-id="611fb-121">**ClassCoNtext** 限定詞會附加至類別，並包含適用于類別中每個實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="611fb-121">The **ClassContext** qualifier is attached to a class and contains information that applies to every instance in the class.</span></span> <span data-ttu-id="611fb-122">例如，在用來儲存登錄提供者所提供之資料的類別中， **ClassCoNtext** 可以是登錄機碼的路徑，其中包含要報告的屬性。</span><span class="sxs-lookup"><span data-stu-id="611fb-122">For example, in a class used to store data supplied by the Registry provider, **ClassContext** can be the path to the registry key that contains the properties to be reported.</span></span>
-   <span data-ttu-id="611fb-123">**PropertyCoNtext** 限定詞會指定與屬性相關的內容特定資訊。</span><span class="sxs-lookup"><span data-stu-id="611fb-123">The **PropertyContext** qualifier specifies context-specific information that pertains to the property.</span></span> <span data-ttu-id="611fb-124">例如，在用來儲存登錄提供者所提供之資料的類別中， **PropertyCoNtext** 會指定屬性要儲存的登錄值名稱。</span><span class="sxs-lookup"><span data-stu-id="611fb-124">For example, in a class used to store data supplied by the Registry provider, **PropertyContext** specifies the name of the registry value to be stored by the property.</span></span>

<span data-ttu-id="611fb-125">這些限定詞可以搭配使用。</span><span class="sxs-lookup"><span data-stu-id="611fb-125">These qualifiers can work together.</span></span> <span data-ttu-id="611fb-126">您可以同時指定 **InstanceCoNtext** 和 **PropertyCoNtext** 值，告知提供者如何處理特定類型的實例。</span><span class="sxs-lookup"><span data-stu-id="611fb-126">You can designate both an **InstanceContext** and **PropertyContext** value to tell the provider how to treat particular types of instances.</span></span> <span data-ttu-id="611fb-127">例如，您可能想要將提供者辨識的實例標示為可讀取，但只有一個可寫入的屬性。</span><span class="sxs-lookup"><span data-stu-id="611fb-127">For example, you might want to mark instances the provider will recognize as readable but having only one writeable property.</span></span>

<span data-ttu-id="611fb-128">最常使用的限定詞是 **PropertyCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="611fb-128">The most common qualifier used is **PropertyContext**.</span></span> <span data-ttu-id="611fb-129">因此，WMI 會將 **DynProps** 限定詞提供為快捷方式。</span><span class="sxs-lookup"><span data-stu-id="611fb-129">Therefore, WMI provides the **DynProps** qualifier as a shortcut.</span></span> <span data-ttu-id="611fb-130">WMI 會將以 **DynProps** 標記的實例中的每個屬性，視為也有 **動態**、 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)和 **PropertyCoNtext** 的限定詞。</span><span class="sxs-lookup"><span data-stu-id="611fb-130">WMI considers each property in an instance marked with **DynProps** to also have the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** qualifiers.</span></span>

 

 



