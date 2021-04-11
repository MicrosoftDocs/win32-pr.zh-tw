---
description: 可轉移元件的一般用途是在系統升級期間準備要重新安裝的產品。
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: 使用可轉移的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35982aafd486a62ce8560e507b8b6caf88e32591
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945756"
---
# <a name="using-transitive-components"></a><span data-ttu-id="f5994-103">使用可轉移的元件</span><span class="sxs-lookup"><span data-stu-id="f5994-103">Using Transitive Components</span></span>

<span data-ttu-id="f5994-104">可轉移元件的一般用途是在系統升級期間準備要重新安裝的產品。</span><span class="sxs-lookup"><span data-stu-id="f5994-104">A typical use for transitive components is to prepare a product to reinstall during a system upgrade.</span></span> <span data-ttu-id="f5994-105">安裝套件的作者會指定在系統升級期間必須交換為具有可轉移屬性的元件。</span><span class="sxs-lookup"><span data-stu-id="f5994-105">The author of the installation package specifies those components that need to be swapped out during a system upgrade as having the transitive attribute.</span></span> <span data-ttu-id="f5994-106">當使用者稍後升級系統時，必須重新安裝產品。</span><span class="sxs-lookup"><span data-stu-id="f5994-106">When the user later upgrades the system, the product must be reinstalled.</span></span> <span data-ttu-id="f5994-107">重新安裝之後，安裝程式會移除先前的元件，並安裝較新的元件，而不需要安裝整個產品。</span><span class="sxs-lookup"><span data-stu-id="f5994-107">Upon this reinstall, the installer removes the earlier components and installs the later components, without having to install the entire product.</span></span>

<span data-ttu-id="f5994-108">**在安裝套件中包含兩個可轉移的元件**</span><span class="sxs-lookup"><span data-stu-id="f5994-108">**To include two transitive components in the installation package**</span></span>

1.  <span data-ttu-id="f5994-109">在安裝套件中包含這兩個可轉移的元件。</span><span class="sxs-lookup"><span data-stu-id="f5994-109">Include both transitive components in the installation package.</span></span>
2.  <span data-ttu-id="f5994-110">將兩個可轉移的元件撰寫成 [元件資料表](component-table.md) ，與一般元件相同。</span><span class="sxs-lookup"><span data-stu-id="f5994-110">Author both transitive components into the [Component table](component-table.md) the same as regular components.</span></span> <span data-ttu-id="f5994-111">每個可轉移的元件都必須在 [元件] 資料行中指定自己的唯一 GUID。</span><span class="sxs-lookup"><span data-stu-id="f5994-111">Each transitive component must have its own unique GUID specified in the ComponentId column.</span></span>
3.  <span data-ttu-id="f5994-112">在元件資料表的 [屬性] 資料行中包含每個可轉移元件的 **msidbComponentAttributesTransitive** 位。</span><span class="sxs-lookup"><span data-stu-id="f5994-112">Include the **msidbComponentAttributesTransitive** bit in the Attributes column of the Component table for each transitive component.</span></span> <span data-ttu-id="f5994-113">如果設定此位，則安裝程式會在重新安裝時重新評估 [條件] 資料行中的語句值。</span><span class="sxs-lookup"><span data-stu-id="f5994-113">If this bit is set, the installer reevaluates the value of the statement in the Condition column upon a reinstall.</span></span>

    <span data-ttu-id="f5994-114">如果值先前是 False，且已變更為 True，則安裝程式會安裝元件。</span><span class="sxs-lookup"><span data-stu-id="f5994-114">If the value was previously False and has changed to True, the installer installs the component.</span></span>

    <span data-ttu-id="f5994-115">如果值先前是 True 且已變更為 False，即使元件有其他產品做為用戶端，安裝程式也會移除該元件。</span><span class="sxs-lookup"><span data-stu-id="f5994-115">If the value was previously True and has changed to False the installer removes the component even if the component has other products as clients.</span></span>

    > [!Note]  
    > <span data-ttu-id="f5994-116">除非已設定可轉移位，否則即使在產品的後續維護安裝中，條件陳述式會評估為 False，仍然會在安裝後啟用元件。</span><span class="sxs-lookup"><span data-stu-id="f5994-116">Unless the transitive bit is set, the component remains enabled once installed even if the conditional statement evaluates to False on a subsequent maintenance installation of the product.</span></span> <span data-ttu-id="f5994-117">條件必須只以電腦狀態為基礎。</span><span class="sxs-lookup"><span data-stu-id="f5994-117">The conditions must be based only on computer states.</span></span> <span data-ttu-id="f5994-118">請勿依據命令列上設定的使用者狀態或屬性來使用 with 條件，因為這可能會導致安裝程式要求不同使用者在每次使用時都必須重新安裝產品。</span><span class="sxs-lookup"><span data-stu-id="f5994-118">Do not use with conditions based on user states or properties set on the command line because this can cause the installer to require a reinstallation of the product on each use by a different user.</span></span>

     

4.  <span data-ttu-id="f5994-119">在控制資料表的 [條件] 欄位中輸入互補的條件運算式，如此一來，當第一個可轉移元件上的條件變更為 False 時，第二個可轉移元件上的條件會變更為 True。</span><span class="sxs-lookup"><span data-stu-id="f5994-119">Enter complementary conditional expressions into the Condition fields of the Control table such that when the condition on the first transitive component changes to False the condition on the second transitive component changes to True.</span></span> <span data-ttu-id="f5994-120">這會導致在重新安裝應用程式時，移除第一個元件和第二個元件的安裝。</span><span class="sxs-lookup"><span data-stu-id="f5994-120">This results in the removal of the first component and installation of the second component upon reinstallation of the application.</span></span>

<span data-ttu-id="f5994-121">若要切換可轉移的元件，必須重新安裝產品。</span><span class="sxs-lookup"><span data-stu-id="f5994-121">A reinstallation of the product is necessary to switch the transitive components.</span></span> <span data-ttu-id="f5994-122">因此，封裝作者必須為使用者提供重新安裝產品的方法，以及設定 [**REINSTALLMODE**](reinstallmode.md) 屬性的模式。</span><span class="sxs-lookup"><span data-stu-id="f5994-122">Package authors therefore need to provide users with a method for reinstalling the product and for setting the modes of the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="f5994-123">基本上，有三種方式可觸發重新安裝：</span><span class="sxs-lookup"><span data-stu-id="f5994-123">There are basically three ways to trigger the reinstallation:</span></span>

-   <span data-ttu-id="f5994-124">藉由撰寫使用 [*完整 UI*](f-gly.md)的封裝，執行並設定透過使用者介面重新安裝。</span><span class="sxs-lookup"><span data-stu-id="f5994-124">Run and configure the reinstallation through the user interface by authoring a package that uses the [*full UI*](f-gly.md).</span></span>
-   <span data-ttu-id="f5994-125">使用 **msiexec/f** 從命令列執行重新安裝，然後從 [ **/f** [命令列] 選項](command-line-options.md)的清單中選取模式。</span><span class="sxs-lookup"><span data-stu-id="f5994-125">Run the reinstallation from the command line by using **msiexec /f** and select the modes from the list for the **/f** [command line option](command-line-options.md).</span></span>
-   <span data-ttu-id="f5994-126">讓應用程式呼叫 [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 或 [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)。</span><span class="sxs-lookup"><span data-stu-id="f5994-126">Have the application call [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) or [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).</span></span>

<span data-ttu-id="f5994-127">此位應僅用於以電腦狀態為基礎的條件。</span><span class="sxs-lookup"><span data-stu-id="f5994-127">The bit should only be used with conditions based on computer states.</span></span> <span data-ttu-id="f5994-128">請勿依據命令列上設定的使用者狀態或屬性來使用 with 條件，因為這可能會導致安裝程式要求不同使用者在每次使用時都必須重新安裝產品。</span><span class="sxs-lookup"><span data-stu-id="f5994-128">Do not use with conditions based on user states or properties set on the command line because this can cause the installer to require a reinstallation of the product on each use by a different user.</span></span>

> [!Note]
> <span data-ttu-id="f5994-129">除非針對元件設定 [屬性] 資料行中的可轉移位，否則即使在 [條件] 資料行中的條件陳述式在產品的後續維護安裝中評估為 False，仍然會在安裝後啟用此元件。</span><span class="sxs-lookup"><span data-stu-id="f5994-129">Unless the Transitive bit in the Attributes column is set for a component, the component remains enabled once installed even if the conditional statement in the Condition column evaluates to False on a subsequent maintenance installation of the product.</span></span>
> 
> <span data-ttu-id="f5994-130">在大部分情況下，如果應用程式包含可轉移的元件，Windows Installer 要求應用程式的來源修復或升級應用程式。</span><span class="sxs-lookup"><span data-stu-id="f5994-130">In most cases, if an application includes transitive components, Windows Installer requires the application's source to repair or upgrade the application.</span></span> <span data-ttu-id="f5994-131">在這些情況下，原始設備製造商所附的系統還原 CD-ROM 無法運作，且需要提供應用程式的實際安裝來源。</span><span class="sxs-lookup"><span data-stu-id="f5994-131">In these cases, the system restoration CD-ROM shipped by an original equipment manufacturer does not work and an actual installation source for the application needs to be provided.</span></span>

 

 

 



