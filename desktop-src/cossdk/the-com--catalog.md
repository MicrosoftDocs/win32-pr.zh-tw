---
description: COM + 目錄會儲存 COM + 應用程式屬性、類別屬性和電腦層級的屬性。 它保證這些屬性之間的一致性，並在這些屬性上提供一般作業。
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: COM + 類別目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970312"
---
# <a name="the-com-catalog"></a><span data-ttu-id="e8517-104">COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="e8517-104">The COM+ Catalog</span></span>

<span data-ttu-id="e8517-105">COM + 目錄會儲存 COM + 應用程式屬性、類別屬性和電腦層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8517-105">The COM+ catalog stores COM+ application attributes, class attributes, and computer-level attributes.</span></span> <span data-ttu-id="e8517-106">它保證這些屬性之間的一致性，並在這些屬性上提供一般作業。</span><span class="sxs-lookup"><span data-stu-id="e8517-106">It guarantees consistency among these attributes and provides common operations on top of these attributes.</span></span>

<span data-ttu-id="e8517-107">COM + 類別目錄會使用兩個不同的存放區，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e8517-107">The COM+ catalog uses two different stores, as follows:</span></span>

-   <span data-ttu-id="e8517-108">COM + 註冊資料庫</span><span class="sxs-lookup"><span data-stu-id="e8517-108">The COM+ registration database</span></span>
-   <span data-ttu-id="e8517-109">Windows 登錄 (**HKEY \_ 類別 \_ 根目錄**) </span><span class="sxs-lookup"><span data-stu-id="e8517-109">The Windows registry (**HKEY\_CLASSES\_ROOT**)</span></span>

<span data-ttu-id="e8517-110">目錄提供這兩個存放區的統一、邏輯觀點，並透過 COM + 系統管理程式庫公開這些存放區。</span><span class="sxs-lookup"><span data-stu-id="e8517-110">The catalog presents a unified, logical view of these two stores and exposes them through the COM+ Administration Library.</span></span> <span data-ttu-id="e8517-111">此程式庫透過指令碼語言提供元件服務系統管理工具的所有功能。</span><span class="sxs-lookup"><span data-stu-id="e8517-111">This library provides, through a scripting language, all the functionality of the Component Services administrative tool.</span></span>

<span data-ttu-id="e8517-112">如果現有的 COM 元件不需要任何新的 COM + 服務，則會在現有的 Windows 登錄中進行查閱。</span><span class="sxs-lookup"><span data-stu-id="e8517-112">For existing COM components that do not require any new COM+ services, lookup occurs in the existing Windows registry.</span></span> <span data-ttu-id="e8517-113">COM + 類別目錄也會針對類型程式庫和介面 proxy/stub 註冊使用 Windows 登錄。</span><span class="sxs-lookup"><span data-stu-id="e8517-113">The COM+ catalog also uses the Windows registry for type library and interface proxy/stub registration.</span></span>

## <a name="split-registration"></a><span data-ttu-id="e8517-114">分割註冊</span><span class="sxs-lookup"><span data-stu-id="e8517-114">Split Registration</span></span>

<span data-ttu-id="e8517-115">針對實際已經存在於服務環境中的現有 COM 元件的新元件 (例如，) 的 MTS 元件，註冊的基本 COM 層面會儲存在 Windows 登錄中，而新的服務和屬性 (例如，已排入佇列的元件) 儲存在 COM + 註冊資料庫中。</span><span class="sxs-lookup"><span data-stu-id="e8517-115">For new components that are actually already existing COM components that are used in the services environment (for example, MTS components), the basic COM aspect of the registration is stored in the Windows registry and new services and attributes (for example, queued components) are stored in the COM+ registration database.</span></span> <span data-ttu-id="e8517-116">這稱為「 *分割註冊*」。</span><span class="sxs-lookup"><span data-stu-id="e8517-116">This is known as a *split registration*.</span></span>

<span data-ttu-id="e8517-117">每個屬性都只會儲存在一個位置： Windows 登錄或 COM + 註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="e8517-117">Each attribute is stored in only one location: either the Windows registry or the COM+ registration database.</span></span> <span data-ttu-id="e8517-118">新的 COM 元件會以獨佔方式在 COM + 註冊資料庫中註冊，並在 Windows 登錄中進行一些重複，讓現有的工具可以使用這些元件。</span><span class="sxs-lookup"><span data-stu-id="e8517-118">New COM components are registered exclusively in the COM+ registration database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

## <a name="transactional-updates-to-the-catalog"></a><span data-ttu-id="e8517-119">目錄的交易式更新</span><span class="sxs-lookup"><span data-stu-id="e8517-119">Transactional Updates to the Catalog</span></span>

<span data-ttu-id="e8517-120">目錄上的某些作業會以交易方式執行。</span><span class="sxs-lookup"><span data-stu-id="e8517-120">Some operations on the catalog are performed in a transactional manner.</span></span> <span data-ttu-id="e8517-121">當您從交易元件叫用 COM + 系統管理程式庫時，會在呼叫元件的交易界限內進行 COM + 註冊資料庫的更新。</span><span class="sxs-lookup"><span data-stu-id="e8517-121">When you invoke the COM+ Administration Library from a transactional component, the updates to the COM+ registration database will take place within the calling component's transaction boundary.</span></span>

<span data-ttu-id="e8517-122">不過，牽涉到其他存放區變更的更新 (例如檔案系統和 Windows 登錄) 並不保證是完全交易。</span><span class="sxs-lookup"><span data-stu-id="e8517-122">However, updates that involve changes to other stores (such as the file system and Windows registry) are not guaranteed to be fully transactional.</span></span> <span data-ttu-id="e8517-123">中止的交易可讓這些存放區的狀態與對另一個或 COM + 註冊資料庫所做的任何變更不一致。</span><span class="sxs-lookup"><span data-stu-id="e8517-123">An aborted transaction can leave these stores in a state that is inconsistent with any changes made to one another or to the COM+ registration database.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8517-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8517-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8517-125">建立 COM + 應用程式的安裝套件</span><span class="sxs-lookup"><span data-stu-id="e8517-125">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="e8517-126">部署應用程式 proxy</span><span class="sxs-lookup"><span data-stu-id="e8517-126">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="e8517-127">COMREPL 複製公用程式</span><span class="sxs-lookup"><span data-stu-id="e8517-127">The COMREPL Replication Utility</span></span>](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



