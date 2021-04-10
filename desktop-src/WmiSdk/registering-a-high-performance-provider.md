---
description: 如同其他執行個體提供者，您可以向 Microsoft Windows&160 註冊高效能的提供者 \# ;Management Instrumentation (WMI) ，方法是建立 \_ \_ Win32Provider 和 \_ \_ InstanceProviderRegistration 類別的實例。
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: 註冊 High-Performance 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026491"
---
# <a name="registering-a-high-performance-provider"></a><span data-ttu-id="d6eaf-103">註冊 High-Performance 提供者</span><span class="sxs-lookup"><span data-stu-id="d6eaf-103">Registering a High-Performance Provider</span></span>

<span data-ttu-id="d6eaf-104">如同其他執行個體提供者，您可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別的實例，向 Microsoft Windows Management Instrumentation (WMI) 註冊高效能的提供者。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-104">Like other instance providers, you register a high-performance provider with Microsoft Windows Management Instrumentation (WMI) by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes.</span></span> <span data-ttu-id="d6eaf-105">**\_ \_ Win32Provider** 實例會定義提供者的實體執行，而 **\_ \_ InstanceProviderRegistration** 實例則會定義提供者的功能集。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-105">The **\_\_Win32Provider** instance defines the provider's physical implementation, and the **\_\_InstanceProviderRegistration** instance defines the provider's feature set.</span></span> <span data-ttu-id="d6eaf-106">如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-106">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="d6eaf-107">下列程式說明如何註冊高效能執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-107">The following procedure describes how to register a high-performance instance provider.</span></span>

<span data-ttu-id="d6eaf-108">**註冊高效能執行個體提供者**</span><span class="sxs-lookup"><span data-stu-id="d6eaf-108">**To register a high-performance instance provider**</span></span>

1.  <span data-ttu-id="d6eaf-109">建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class describing the provider.</span></span>

    <span data-ttu-id="d6eaf-110">務必將 **ClientLoadableCLSID** 屬性加入至 [**\_ \_ Win32Provider**](--win32provider.md)實例。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-110">Be sure to add a **ClientLoadableCLSID** property to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span> <span data-ttu-id="d6eaf-111">如果提供者和用戶端都位於相同的電腦上，WMI 會使用 **ClientLoadableCLSID** 做為類別識別碼，將處理常式載入至用戶端。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-111">If both the provider and client reside on the same computer, WMI loads the provider in-process to the client using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="d6eaf-112">當提供者和用戶端位於不同的電腦上時，WMI 會將提供者載入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-112">When the provider and client reside on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="d6eaf-113">WMI 也會使用 **ClientLoadableCLSID** 來支援重新整理作業。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-113">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

2.  <span data-ttu-id="d6eaf-114">建立 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別的實例，以描述提供者的功能集。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-114">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="d6eaf-115">請務必使用 [**動態**](dynamic-qualifier.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號來標記類別。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-115">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="d6eaf-116">**動態** 限定詞表示 WMI 應該使用提供者來取出類別實例。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-116">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="d6eaf-117">**提供者** 辨識符號會指定 WMI 應使用的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-117">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

    <span data-ttu-id="d6eaf-118">高效能提供者也需要為作業、列舉作業或兩者提供狀態支援。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-118">A high-performance provider also needs to state support for operations, enumeration operations, or both.</span></span> <span data-ttu-id="d6eaf-119">請務必在您的執行中使用 **SupportsGet** 和 **SupportsEnumeration** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-119">Make sure you use the **SupportsGet** and **SupportsEnumeration** properties in your implementation.</span></span>

<span data-ttu-id="d6eaf-120">下列程式碼範例示範如何為高效能提供者執行 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)類別。</span><span class="sxs-lookup"><span data-stu-id="d6eaf-120">The following code example shows you how to implement the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes for a high-performance provider.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a><span data-ttu-id="d6eaf-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6eaf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6eaf-122">讓執行個體提供者成為 High-Performance 提供者</span><span class="sxs-lookup"><span data-stu-id="d6eaf-122">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



