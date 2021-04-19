---
description: 當您指定安裝的元件時，套件作者應遵循將應用程式組織成元件中所述之元件組織的一般規則。
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: 變更元件程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7531b4a38312d4abed038b612c4292c44af8e967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998490"
---
# <a name="changing-the-component-code"></a><span data-ttu-id="71173-103">變更元件程式碼</span><span class="sxs-lookup"><span data-stu-id="71173-103">Changing the Component Code</span></span>

<span data-ttu-id="71173-104">當您指定安裝的 [元件](windows-installer-components.md) 時，套件作者應遵循將 [應用程式組織成元件](organizing-applications-into-components.md)中所述之元件組織的一般規則。</span><span class="sxs-lookup"><span data-stu-id="71173-104">When specifying the [components](windows-installer-components.md) for an installation, package authors should follow the general rules for component organization described in [Organizing Applications into Components](organizing-applications-into-components.md).</span></span> <span data-ttu-id="71173-105">作者可能需要引進新元件或修改現有的元件。</span><span class="sxs-lookup"><span data-stu-id="71173-105">Authors may need to introduce new components or modify existing components.</span></span> <span data-ttu-id="71173-106">如果新增、移除或修改資源實際上會建立新的元件，則元件程式碼也必須變更。</span><span class="sxs-lookup"><span data-stu-id="71173-106">If the addition, removal, or modification of resources effectively creates a new component, then the component code must also be changed.</span></span>

## <a name="creating-a-new-component"></a><span data-ttu-id="71173-107">建立新元件</span><span class="sxs-lookup"><span data-stu-id="71173-107">Creating a New Component</span></span>

<span data-ttu-id="71173-108">引進新元件，並在進行下列任何變更時，為它指派唯一的元件程式碼：</span><span class="sxs-lookup"><span data-stu-id="71173-108">Introduce a new component and assign it a unique component code when making any of the following changes:</span></span>

-   <span data-ttu-id="71173-109">測試未顯示的任何變更與舊版元件相容。</span><span class="sxs-lookup"><span data-stu-id="71173-109">Any change that has not been shown by testing to be compatible with previous versions of the component.</span></span> <span data-ttu-id="71173-110">在此情況下，您也必須變更元件中每個資源的名稱或目標位置。</span><span class="sxs-lookup"><span data-stu-id="71173-110">In this case, you must also change the name or target location of every resource in the component.</span></span>
-   <span data-ttu-id="71173-111">元件中任何檔案、登錄機碼、快捷方式或其他資源之名稱或目標位置的變更。</span><span class="sxs-lookup"><span data-stu-id="71173-111">A change in the name or target location of any file, registry key, shortcut, or other resource in the component.</span></span> <span data-ttu-id="71173-112">在此情況下，您也必須變更元件中每個資源的名稱或目標位置。</span><span class="sxs-lookup"><span data-stu-id="71173-112">In this case, you must also change the name or target location of every resource in the component.</span></span>
-   <span data-ttu-id="71173-113">從元件新增或移除任何檔案、登錄機碼、快捷方式或其他資源。</span><span class="sxs-lookup"><span data-stu-id="71173-113">The addition or removal of any file, registry key, shortcut, or other resource from the component.</span></span> <span data-ttu-id="71173-114">在此情況下，您也必須變更元件中每個資源的名稱或目標位置。</span><span class="sxs-lookup"><span data-stu-id="71173-114">In this case, you must also change the name or target location of every resource in the component.</span></span>
-   <span data-ttu-id="71173-115">將32位元件重新編譯成64位元件。</span><span class="sxs-lookup"><span data-stu-id="71173-115">Recompiling a 32-bit component into a 64-bit component.</span></span>

<span data-ttu-id="71173-116">引進新元件時，作者必須執行下列其中一項動作，以確保元件不會與任何現有的元件衝突：</span><span class="sxs-lookup"><span data-stu-id="71173-116">When introducing a new component, authors need to do one of the following to ensure that the component does not conflict with any existing components:</span></span>

-   <span data-ttu-id="71173-117">將任何可能安裝的資源名稱或目標位置，變更為其他元件的相同名稱和目標位置。</span><span class="sxs-lookup"><span data-stu-id="71173-117">Change the name or target location of any resource that may be installed under the same name and target location by another component.</span></span>
-   <span data-ttu-id="71173-118">否則，保證新元件永遠不會安裝在與另一個元件相同的資料夾中，而該元件具有一般名稱和位置下的資源。</span><span class="sxs-lookup"><span data-stu-id="71173-118">Otherwise guarantee that the new component is never installed into the same folder as another component which has a resource under a common name and location.</span></span> <span data-ttu-id="71173-119">這包括具有相同檔案名的檔案當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="71173-119">This includes localized versions of files with the same file name.</span></span> <span data-ttu-id="71173-120">如需詳細資訊，請參閱 [元件規則中斷時，會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)。</span><span class="sxs-lookup"><span data-stu-id="71173-120">For more information, see [What happens if the component rules are broken?](what-happens-if-the-component-rules-are-broken.md).</span></span>
-   <span data-ttu-id="71173-121">變更現有元件的元件程式碼時，也請變更元件中每個檔案、登錄機碼、快捷方式和其他資源的名稱或目標位置。</span><span class="sxs-lookup"><span data-stu-id="71173-121">When changing the component code of an existing component, also change the name or target location of every file, registry key, shortcut, and other resource in the component.</span></span>

### <a name="creating-a-new-version-of-a-component"></a><span data-ttu-id="71173-122">建立新版本的元件</span><span class="sxs-lookup"><span data-stu-id="71173-122">Creating a New Version of a Component</span></span>

<span data-ttu-id="71173-123">新版本的元件會被指派與另一個現有元件相同的元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="71173-123">A new version of a component is assigned the same component code as another existing component.</span></span> <span data-ttu-id="71173-124">在下列情況下，修改元件而不變更元件程式碼是選擇性的：</span><span class="sxs-lookup"><span data-stu-id="71173-124">Modifying a component without changing the component code is only optional in the following cases:</span></span>

-   <span data-ttu-id="71173-125">對元件所做的變更已經過測試，可與所有舊版元件回溯相容。</span><span class="sxs-lookup"><span data-stu-id="71173-125">The changes to the component have been proven by testing to be backward compatible with all previous versions of the component.</span></span>
-   <span data-ttu-id="71173-126">作者可以保證新版本的元件永遠不會安裝在系統上，因為它會與舊版元件或需要舊版的應用程式發生衝突。</span><span class="sxs-lookup"><span data-stu-id="71173-126">The author can guarantee that the new version of the component will never be installed on a system where it would conflict with previous versions of the component or applications requiring a previous version.</span></span> <span data-ttu-id="71173-127">如需詳細資訊，請參閱 [元件規則中斷時，會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)。</span><span class="sxs-lookup"><span data-stu-id="71173-127">For more information, see [What happens if the component rules are broken?](what-happens-if-the-component-rules-are-broken.md).</span></span>

<span data-ttu-id="71173-128">當新版本的元件產生兩個元件共用資源時（例如登錄值、檔案或快捷方式），不能變更元件的元件代碼。</span><span class="sxs-lookup"><span data-stu-id="71173-128">The component code of a new version of a component must not be changed when it would result in two components sharing resources, such as registry values, files, or shortcuts.</span></span>

 

 



