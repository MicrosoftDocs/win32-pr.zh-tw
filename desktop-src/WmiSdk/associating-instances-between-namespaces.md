---
description: 相關檢視類別可讓您在位於不同命名空間的類別上，使用查詢的 ASSOCIATORS OF。
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: 在命名空間之間建立實例的關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319467"
---
# <a name="associating-instances-between-namespaces"></a><span data-ttu-id="4627e-103">在命名空間之間建立實例的關聯</span><span class="sxs-lookup"><span data-stu-id="4627e-103">Associating Instances Between Namespaces</span></span>

<span data-ttu-id="4627e-104">相關檢視類別可讓您在位於不同命名空間的類別上，使用查詢 [的 associators of](associators-of-statement.md) 。</span><span class="sxs-lookup"><span data-stu-id="4627e-104">An association view class allows you to use [ASSOCIATORS OF](associators-of-statement.md) queries on classes that reside in different namespaces.</span></span>

<span data-ttu-id="4627e-105">下列程式描述如何在命名空間之間建立實例的關聯。</span><span class="sxs-lookup"><span data-stu-id="4627e-105">The following procedure describes how to associate instances between namespaces.</span></span>

<span data-ttu-id="4627e-106">**若要在命名空間之間建立實例的關聯**</span><span class="sxs-lookup"><span data-stu-id="4627e-106">**To associate instances between namespaces**</span></span>

1.  <span data-ttu-id="4627e-107">使用 [**關聯**](meta-qualifiers.md) 字串辨識符號來開始您的類別定義。</span><span class="sxs-lookup"><span data-stu-id="4627e-107">Begin your class definition with the [**Association**](meta-qualifiers.md) string qualifier.</span></span>

    <span data-ttu-id="4627e-108">**JoinOn**、 [**Association**](meta-qualifiers.md)和 **Union** 限定詞都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="4627e-108">The **JoinOn**, [**Association**](meta-qualifiers.md), and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="4627e-109">建立查詢，以使用 [**ViewSources**](viewsources-qualifier.md) 限定詞來定義 view 類別中所使用的來源實例。</span><span class="sxs-lookup"><span data-stu-id="4627e-109">Create the queries that define source instances used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="4627e-110">使用 [**ViewSpaces**](viewspaces-qualifier.md) 限定詞來定義來源實例所在之命名空間的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="4627e-110">Define the names and location of the namespaces in which the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="4627e-111">使用 [**PropertySources**](propertysources-qualifier.md) 限定詞，在您的 [關聯] view 類別中定義您想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="4627e-111">Define the properties you want in your association view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="4627e-112">如有必要，您可以使用 [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) 限定詞，將任何屬性標記為屬於來源類別。</span><span class="sxs-lookup"><span data-stu-id="4627e-112">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="4627e-113">使用 **直接** 辨識符號標記任何相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="4627e-113">Tag any relevant properties with the **Direct** qualifier.</span></span>

    <span data-ttu-id="4627e-114">**直接** 辨識符號會防止 View 提供者將標記的關聯參考對應到視圖參考。</span><span class="sxs-lookup"><span data-stu-id="4627e-114">The **Direct** qualifier prevents the View Provider from mapping the tagged association reference to a view reference.</span></span>

<span data-ttu-id="4627e-115">下列程式碼範例示範如何建立相關檢視類別。</span><span class="sxs-lookup"><span data-stu-id="4627e-115">The following code examples show how to create association view classes.</span></span>

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



