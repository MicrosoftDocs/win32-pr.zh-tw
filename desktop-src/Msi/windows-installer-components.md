---
description: 元件是要安裝的應用程式或產品的一部分。
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Windows Installer 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944527"
---
# <a name="windows-installer-components"></a><span data-ttu-id="780b2-103">Windows Installer 元件</span><span class="sxs-lookup"><span data-stu-id="780b2-103">Windows Installer Components</span></span>

<span data-ttu-id="780b2-104">元件是要安裝的應用程式或產品的一部分。</span><span class="sxs-lookup"><span data-stu-id="780b2-104">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="780b2-105">元件的範例包括單一檔案、相關檔案的群組、COM 物件、註冊、登錄機碼、快捷方式、資源、群組在目錄中的程式庫，或共用程式碼段（例如 MFC 或 DAO）。</span><span class="sxs-lookup"><span data-stu-id="780b2-105">Examples of components include single files, a group of related files, COM objects, registration, registry keys, shortcuts, resources, libraries grouped into a directory, or shared pieces of code such as MFC or DAO.</span></span>

<span data-ttu-id="780b2-106">安裝程式服務會以單一一致的部分形式安裝或移除元件。</span><span class="sxs-lookup"><span data-stu-id="780b2-106">The installer service installs or removes a component as a single coherent piece.</span></span> <span data-ttu-id="780b2-107">它會依 [元件資料表](component-table.md)的 [元件識別碼] 資料行中指定的個別元件識別碼 GUID 來追蹤每個元件。</span><span class="sxs-lookup"><span data-stu-id="780b2-107">It tracks every component by the respective component ID GUID specified in the ComponentId column of the [Component table](component-table.md).</span></span>

> [!Note]  
> <span data-ttu-id="780b2-108">共用相同元件識別碼的兩個元件會視為相同元件的多個實例，不論其實際內容為何。</span><span class="sxs-lookup"><span data-stu-id="780b2-108">Two components that share the same component ID are treated as multiple instances of the same component regardless of their actual content.</span></span> <span data-ttu-id="780b2-109">只有任何元件的單一實例會安裝在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="780b2-109">Only a single instance of any component is installed on a user's computer.</span></span> <span data-ttu-id="780b2-110">因此，有幾個功能或應用程式可能會共用某些元件。</span><span class="sxs-lookup"><span data-stu-id="780b2-110">Several features or applications may therefore share some components.</span></span>

 

<span data-ttu-id="780b2-111">因為通常會共用元件，所以安裝套件的作者在指定功能或應用程式的元件時，必須遵守嚴格的規則。</span><span class="sxs-lookup"><span data-stu-id="780b2-111">Because components are commonly shared, the author of an installation package must follow strict rules when specifying the components of a feature or application.</span></span> <span data-ttu-id="780b2-112">這對於 Windows Installer 參考計數機制的正確作業而言是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="780b2-112">This is essential for the correct operation of the Windows Installer reference-counting mechanism.</span></span> <span data-ttu-id="780b2-113">如需詳細資訊，請參閱將 [應用程式組織成元件](organizing-applications-into-components.md)。</span><span class="sxs-lookup"><span data-stu-id="780b2-113">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="780b2-114">簡單來說，這些規則包括：</span><span class="sxs-lookup"><span data-stu-id="780b2-114">In brief, these rules are:</span></span>

-   <span data-ttu-id="780b2-115">每個元件都必須儲存在單一資料夾中。</span><span class="sxs-lookup"><span data-stu-id="780b2-115">Each component must be stored in a single folder.</span></span>
-   <span data-ttu-id="780b2-116">不應將任何檔案、登錄專案、快捷方式或其他資源以一個以上的元件的成員形式傳送。</span><span class="sxs-lookup"><span data-stu-id="780b2-116">No file, registry entry, shortcut, or other resources should ever be shipped as a member of more than one component.</span></span> <span data-ttu-id="780b2-117">這適用于各產品、產品版本和公司。</span><span class="sxs-lookup"><span data-stu-id="780b2-117">This applies across products, product versions, and companies.</span></span>

<span data-ttu-id="780b2-118">如需使用元件的詳細資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="780b2-118">For more information about using components, see</span></span>

-   [<span data-ttu-id="780b2-119">安裝遺失的元件</span><span class="sxs-lookup"><span data-stu-id="780b2-119">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="780b2-120">安裝永久元件、檔案、字型、登錄機碼</span><span class="sxs-lookup"><span data-stu-id="780b2-120">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
-   [<span data-ttu-id="780b2-121">使用限定元件</span><span class="sxs-lookup"><span data-stu-id="780b2-121">Using Qualified Components</span></span>](using-qualified-components.md)
-   [<span data-ttu-id="780b2-122">使用可轉移的元件</span><span class="sxs-lookup"><span data-stu-id="780b2-122">Using Transitive Components</span></span>](using-transitive-components.md)
-   [<span data-ttu-id="780b2-123">使用功能和元件</span><span class="sxs-lookup"><span data-stu-id="780b2-123">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="780b2-124">撰寫大型封裝</span><span class="sxs-lookup"><span data-stu-id="780b2-124">Authoring a Large Package</span></span>](authoring-a-large-package.md)
-   [<span data-ttu-id="780b2-125">檢查功能、元件、檔案的安裝</span><span class="sxs-lookup"><span data-stu-id="780b2-125">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
-   [<span data-ttu-id="780b2-126">搜尋中斷的功能或元件</span><span class="sxs-lookup"><span data-stu-id="780b2-126">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
-   [<span data-ttu-id="780b2-127">發佈產品、功能和元件</span><span class="sxs-lookup"><span data-stu-id="780b2-127">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)

 

 



