---
description: COM + 應用程式是元件服務的管理和安全性主要單位，由一組通常會執行相關功能的 COM 元件組成。
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: COM + 應用程式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106975581"
---
# <a name="com-application-overview"></a><span data-ttu-id="4ed5c-103">COM + 應用程式總覽</span><span class="sxs-lookup"><span data-stu-id="4ed5c-103">COM+ Application Overview</span></span>

<span data-ttu-id="4ed5c-104">COM + 應用程式是元件服務的管理和安全性主要單位，由一組通常會執行相關功能的 COM 元件組成。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-104">A COM+ application is the primary unit of administration and security for Component Services and consists of a group of COM components that generally perform related functions.</span></span> <span data-ttu-id="4ed5c-105">這些元件會進一步由介面和方法所組成，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-105">These components further consist of interfaces and methods, as shown in the following illustration.</span></span>

![顯示方塊內介面和方法的圖表，以 COM + 應用程式內元件內部介面內的方法順序顯示。](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

<span data-ttu-id="4ed5c-107">您可以使用 [元件服務] 系統管理工具來建立新的 COM + 應用程式、將元件新增至應用程式，以及設定應用程式及其元件的屬性。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-107">You can use the Component Services administrative tool to create new COM+ applications, add components to applications, and set the attributes for an application and its components.</span></span>

<span data-ttu-id="4ed5c-108">藉由將 COM 元件的邏輯群組建立為 COM + 應用程式，您可以利用 COM + 的下列優點：</span><span class="sxs-lookup"><span data-stu-id="4ed5c-108">By creating logical groups of COM components as COM+ applications, you can take advantage of the following benefits of COM+:</span></span>

-   <span data-ttu-id="4ed5c-109">COM 元件的部署範圍。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-109">A deployment scope for COM components.</span></span>
-   <span data-ttu-id="4ed5c-110">COM 元件的一般設定範圍，包括安全性界限和佇列。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-110">A common configuration scope for COM components, including security boundaries and queuing.</span></span>
-   <span data-ttu-id="4ed5c-111">元件開發人員未提供的元件屬性儲存 (例如，交易和同步處理) 。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-111">Storage of component attributes not provided by the component developer (for example, transactions and synchronization).</span></span>
-   <span data-ttu-id="4ed5c-112">元件動態連結程式庫 (Dll) 載入至進程 (DLLHost.exe 視需要) 。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-112">Component dynamic-link libraries (DLLs) loaded into processes (DLLHost.exe) on demand.</span></span>
-   <span data-ttu-id="4ed5c-113">裝載元件的受控伺服器進程。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-113">Managed server processes to host components.</span></span>
-   <span data-ttu-id="4ed5c-114">建立和管理元件所使用的執行緒。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-114">Creation and management of threads used by components.</span></span>
-   <span data-ttu-id="4ed5c-115">存取資源機的內容物件，可讓取得的資源自動與內容產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4ed5c-115">Access to the context object for resource dispensers, allowing acquired resources to be automatically associated with the context.</span></span> <span data-ttu-id="4ed5c-116"> (需有關 COM 元件和內容的詳細資訊，請參閱 [Com +](com--contexts.md)內容。 ) </span><span class="sxs-lookup"><span data-stu-id="4ed5c-116">(For more information on COM components and contexts, see [COM+ Contexts](com--contexts.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ed5c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ed5c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed5c-118">開發 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="4ed5c-118">Developing COM+ Applications</span></span>](developing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="4ed5c-119">COM + 應用程式的元件</span><span class="sxs-lookup"><span data-stu-id="4ed5c-119">Parts of a COM+ Application</span></span>](parts-of-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="4ed5c-120">COM + 應用程式的類型</span><span class="sxs-lookup"><span data-stu-id="4ed5c-120">Types of COM+ Applications</span></span>](types-of-com--applications.md)
</dt> </dl>

 

 



