---
description: Windows Vista 軟體發展工具組和 Windows XP Tablet PC Edition 開發工具組可讓您為必須存取遠端應用程式的 Tablet PC 使用者，建立具備筆墨功能的 web 應用程式。
ms.assetid: 4ba1ab4b-57d2-40da-a7c7-2402f8845ff5
title: Web 上的筆墨
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3584fdc0f19cbf9ac1a60e8f1607971165077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112316"
---
# <a name="ink-on-the-web"></a><span data-ttu-id="33de2-103">Web 上的筆墨</span><span class="sxs-lookup"><span data-stu-id="33de2-103">Ink on the Web</span></span>

<span data-ttu-id="33de2-104">Windows Vista 軟體發展工具組和 Windows XP Tablet PC Edition 開發工具組可讓您為必須存取遠端應用程式的 Tablet PC 使用者，建立具備筆墨功能的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="33de2-104">The Windows Vista Software Development Kit and Windows XP Tablet PC Edition Development Kit allow you to create ink-enabled web applications for Tablet PC users who must access remote applications.</span></span> <span data-ttu-id="33de2-105">有兩個基本技術可以完成這項操作：一個是無觸控部署，可讓您從 Web 或檔案伺服器部署 .NET 應用程式，而另一個則是使用 Windows Forms 控制項來建立具備筆墨功能的網頁。</span><span class="sxs-lookup"><span data-stu-id="33de2-105">There are two basic techniques for accomplishing this: one is no-touch deployment, which allows .NET applications to be deployed from a Web or file server, and the other is to create ink-enabled Web pages with Windows Forms controls.</span></span> <span data-ttu-id="33de2-106">在這兩種情況下，會在用戶端上處理筆墨，而不是在伺服器上處理。</span><span class="sxs-lookup"><span data-stu-id="33de2-106">In both cases, the ink is handled on the client, rather than the server.</span></span> <span data-ttu-id="33de2-107">請注意，Web 不支援 COM API。</span><span class="sxs-lookup"><span data-stu-id="33de2-107">Note that the COM API is not supported for the Web.</span></span>

<span data-ttu-id="33de2-108">若要在 Web 上使用用戶端處理，您必須瞭解 .NET 安全性模型，以及在部分信任下運作的方式對您的應用程式有何影響。</span><span class="sxs-lookup"><span data-stu-id="33de2-108">To use client-side processing over the Web, you need to understand the .NET security model and how operating under partial trust affects your application.</span></span> <span data-ttu-id="33de2-109">基於這個理由，也會討論 Tablet PC 應用程式的安全性與信任。</span><span class="sxs-lookup"><span data-stu-id="33de2-109">For this reason, security and trust for Tablet PC applications is discussed as well.</span></span>

<span data-ttu-id="33de2-110">下列主題包含有關建立啟用筆墨之 Web 應用程式之各種方式的注意事項。</span><span class="sxs-lookup"><span data-stu-id="33de2-110">The following topics contain notes on various ways of creating ink-enabled Web applications.</span></span>

-   [<span data-ttu-id="33de2-111">無觸控部署</span><span class="sxs-lookup"><span data-stu-id="33de2-111">No Touch Deployment</span></span>](no-touch-deployment.md)
-   [<span data-ttu-id="33de2-112">Web 控制項</span><span class="sxs-lookup"><span data-stu-id="33de2-112">Web Controls</span></span>](web-controls.md)
-   [<span data-ttu-id="33de2-113">啟用筆墨的 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="33de2-113">Ink-Enabled Web Applications</span></span>](ink-enabled-web-applications.md)
-   [<span data-ttu-id="33de2-114">安全性與信任</span><span class="sxs-lookup"><span data-stu-id="33de2-114">Security and Trust</span></span>](security-and-trust.md)

 

 



