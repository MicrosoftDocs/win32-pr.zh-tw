---
description: 建立 COM + 應用程式
ms.assetid: 32828d4d-aa98-4e6a-b7de-2ec832024517
title: 建立 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42a4b7ad18dab3f7163f527626322e05671e7be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995807"
---
# <a name="creating-com-applications"></a><span data-ttu-id="1051a-103">建立 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="1051a-103">Creating COM+ Applications</span></span>

<span data-ttu-id="1051a-104">本節說明如何建立新的 (空白) COM + 應用程式，然後將元件新增至該應用程式。</span><span class="sxs-lookup"><span data-stu-id="1051a-104">This section describes how to create a new (empty) COM+ application and then add components to that application.</span></span> <span data-ttu-id="1051a-105">它也會說明如何將 COM 元件加入至現有的 COM + 應用程式，並將其從現有的 COM + 應用程式中移除，以及如何在 COM + 應用程式之間移動和複製元件至另一個。</span><span class="sxs-lookup"><span data-stu-id="1051a-105">It also describes how to add COM components to, and remove them from, existing COM+ applications, and how to move and copy components from one COM+ application to another.</span></span>



| <span data-ttu-id="1051a-106">主題</span><span class="sxs-lookup"><span data-stu-id="1051a-106">Topic</span></span>                                                                                                       | <span data-ttu-id="1051a-107">描述</span><span class="sxs-lookup"><span data-stu-id="1051a-107">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1051a-108">建立新的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="1051a-108">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)<br/>                           | <span data-ttu-id="1051a-109">說明如何建立新的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1051a-109">Describes how to create a new COM+ application.</span></span><br/>                         |
| [<span data-ttu-id="1051a-110">安裝新元件</span><span class="sxs-lookup"><span data-stu-id="1051a-110">Installing New Components</span></span>](installing-new-components.md)<br/>                                       | <span data-ttu-id="1051a-111">描述如何安裝新元件。</span><span class="sxs-lookup"><span data-stu-id="1051a-111">Describes how to install new components.</span></span><br/>                                |
| [<span data-ttu-id="1051a-112">匯入元件</span><span class="sxs-lookup"><span data-stu-id="1051a-112">Importing Components</span></span>](importing-components.md)<br/>                                                 | <span data-ttu-id="1051a-113">說明如何匯入元件。</span><span class="sxs-lookup"><span data-stu-id="1051a-113">Describes how to import components.</span></span><br/>                                     |
| [<span data-ttu-id="1051a-114">從 COM + 應用程式移除元件</span><span class="sxs-lookup"><span data-stu-id="1051a-114">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)<br/> | <span data-ttu-id="1051a-115">描述如何從 COM + 應用程式刪除元件。</span><span class="sxs-lookup"><span data-stu-id="1051a-115">Describes how to delete a component from a COM+ application.</span></span><br/>            |
| [<span data-ttu-id="1051a-116">移動元件</span><span class="sxs-lookup"><span data-stu-id="1051a-116">Moving Components</span></span>](moving-components.md)<br/>                                                       | <span data-ttu-id="1051a-117">說明如何將元件從一個 COM + 應用程式移到另一個 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1051a-117">Describes how to move a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="1051a-118">複製元件</span><span class="sxs-lookup"><span data-stu-id="1051a-118">Copying Components</span></span>](copying-components.md)<br/>                                                     | <span data-ttu-id="1051a-119">說明如何將元件從一個 COM + 應用程式複製到另一個 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1051a-119">Describes how to copy a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="1051a-120">刪除 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="1051a-120">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)<br/>                                   | <span data-ttu-id="1051a-121">描述如何刪除 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1051a-121">Describes how to delete a COM+ application.</span></span><br/>                             |



 

<span data-ttu-id="1051a-122">如需本節所述程式的概念資訊，請參閱 [Com + 應用程式總覽](com--application-overview.md) 和 [部署 Com + 應用程式](deploying-com--applications.md)。</span><span class="sxs-lookup"><span data-stu-id="1051a-122">For conceptual information on the procedures described in this section, see [COM+ Application Overview](com--application-overview.md) and [Deploying COM+ Applications](deploying-com--applications.md).</span></span>

<span data-ttu-id="1051a-123">如需有關匯出和安裝 COM + 應用程式之管理工作的程式資訊，請參閱《元件服務系統管理員指南》中的「安裝 COM + 應用程式」。</span><span class="sxs-lookup"><span data-stu-id="1051a-123">For procedural information on the administrative tasks involved in exporting and installing COM+ applications, see "Installing COM+ Applications" in the Component Services Administrator's Guide.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1051a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="1051a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1051a-125">自動化 COM + 管理</span><span class="sxs-lookup"><span data-stu-id="1051a-125">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="1051a-126">設定 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="1051a-126">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="1051a-127">將 MTS 套件轉換為 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="1051a-127">Conversion of MTS Packages to COM+ Applications</span></span>](conversion-of-mts-packages-to-com--applications.md)
</dt> </dl>

 

 




