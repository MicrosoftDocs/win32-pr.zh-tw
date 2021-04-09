---
title: 容器和伺服器
description: 容器和伺服器
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840788"
---
# <a name="containers-and-servers"></a><span data-ttu-id="7163e-103">容器和伺服器</span><span class="sxs-lookup"><span data-stu-id="7163e-103">Containers and Servers</span></span>

<span data-ttu-id="7163e-104">複合檔案應用程式有兩種基本類型：容器應用程式和伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="7163e-104">Compound document applications are of two basic types: container applications and server applications.</span></span> <span data-ttu-id="7163e-105">OLE 容器應用程式可讓使用者建立、編輯、儲存和取出複合檔案。</span><span class="sxs-lookup"><span data-stu-id="7163e-105">OLE container applications provide users with the ability to create, edit, save, and retrieve compound documents.</span></span> <span data-ttu-id="7163e-106">OLE 伺服器應用程式會提供使用者方法來建立檔和其他資料表示，以連結或內嵌的形式包含在容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="7163e-106">OLE server applications provide users with the means to create documents and other data representations that can be contained as either links or embeddings in container applications.</span></span> <span data-ttu-id="7163e-107">OLE 應用程式可以是容器應用程式、伺服器應用程式或兩者。</span><span class="sxs-lookup"><span data-stu-id="7163e-107">An OLE application can be a container application, a server application, or both.</span></span>

<span data-ttu-id="7163e-108">OLE server 應用程式的執行方式也不同，因為它們是實作為同 *進程伺服器* 或 *本機伺服器*。</span><span class="sxs-lookup"><span data-stu-id="7163e-108">OLE server applications also differ in whether they are implemented as *in-process servers* or *local servers*.</span></span> <span data-ttu-id="7163e-109">同進程伺服器是在容器應用程式的進程空間中執行 (DLL) 的動態連結程式庫。</span><span class="sxs-lookup"><span data-stu-id="7163e-109">An in-process server is a dynamic link library (DLL) that runs in the container application's process space.</span></span> <span data-ttu-id="7163e-110">您只能從容器應用程式內執行同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="7163e-110">You can run an in-process server only from within the container application.</span></span>

> [!Note]  
> <span data-ttu-id="7163e-111">未來的 OLE 版本會啟用跨電腦界限的連結和內嵌，讓一部電腦上的容器應用程式能夠使用由另一部電腦上執行的 *遠端伺服器* 所提供的複合檔案物件。</span><span class="sxs-lookup"><span data-stu-id="7163e-111">Future releases of OLE will enable linking and embedding across computer boundaries, so that a container application on one computer will be able to use a compound document object provided by a *remote server* running on another computer.</span></span> <span data-ttu-id="7163e-112">從容器應用程式的觀點來看，在它自己的進程空間中執行的任何 OLE 伺服器應用程式（不論是在同一部電腦或遠端電腦上）都是 *processÂ伺服器*。</span><span class="sxs-lookup"><span data-stu-id="7163e-112">From a container application's point of view, any OLE server application that runs in its own process space, whether on the same computer or a remote computer, is an *out-of-processÂ server*.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7163e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="7163e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7163e-114">複合檔案</span><span class="sxs-lookup"><span data-stu-id="7163e-114">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="7163e-115">同進程伺服器</span><span class="sxs-lookup"><span data-stu-id="7163e-115">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




