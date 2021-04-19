---
description: 您可以開發應用程式來執行需要系統管理員許可權，但以標準使用者身分執行的作業。
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: 開發需要系統管理員許可權的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977081"
---
# <a name="developing-applications-that-require-administrator-privilege"></a><span data-ttu-id="c7c8e-103">開發需要系統管理員許可權的應用程式</span><span class="sxs-lookup"><span data-stu-id="c7c8e-103">Developing Applications that Require Administrator Privilege</span></span>

<span data-ttu-id="c7c8e-104">您可以開發應用程式來執行需要系統管理員許可權，但以標準使用者身分執行的作業。</span><span class="sxs-lookup"><span data-stu-id="c7c8e-104">It is possible to develop an application that performs operations that require administrator privilege yet runs as a standard user.</span></span>

<span data-ttu-id="c7c8e-105">有幾個模型可以完成這項程式。</span><span class="sxs-lookup"><span data-stu-id="c7c8e-105">There are several models for accomplishing this.</span></span>



| <span data-ttu-id="c7c8e-106">主題</span><span class="sxs-lookup"><span data-stu-id="c7c8e-106">Topic</span></span>                                                                | <span data-ttu-id="c7c8e-107">描述</span><span class="sxs-lookup"><span data-stu-id="c7c8e-107">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7c8e-108">提高許可權的工作模型</span><span class="sxs-lookup"><span data-stu-id="c7c8e-108">Elevated Task Model</span></span>](elevated-task-model.md)                       | <span data-ttu-id="c7c8e-109">以標準使用者身分執行的應用程式會啟動排程工作，以執行需要系統管理員許可權的作業。</span><span class="sxs-lookup"><span data-stu-id="c7c8e-109">An application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>                                                                     |
| [<span data-ttu-id="c7c8e-110">作業系統服務模型</span><span class="sxs-lookup"><span data-stu-id="c7c8e-110">Operating System Service Model</span></span>](operating-system-service-model.md) | <span data-ttu-id="c7c8e-111">以標準使用者的形式執行的應用程式會使用 [遠端程序呼叫](/windows/desktop/Rpc/rpc-start-page)（ (RPC) ）與以 **系統** 執行的服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="c7c8e-111">An application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>                                              |
| [<span data-ttu-id="c7c8e-112">系統管理員訊息代理程式模型</span><span class="sxs-lookup"><span data-stu-id="c7c8e-112">Administrator Broker Model</span></span>](administrator-broker-model.md)         | <span data-ttu-id="c7c8e-113">應用程式分成兩個程式。</span><span class="sxs-lookup"><span data-stu-id="c7c8e-113">The application is divided into two programs.</span></span> <span data-ttu-id="c7c8e-114">其中一個程式是以標準使用者身分執行，另一個則以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="c7c8e-114">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>                                                          |
| [<span data-ttu-id="c7c8e-115">系統管理員 COM 物件模型</span><span class="sxs-lookup"><span data-stu-id="c7c8e-115">Administrator COM Object Model</span></span>](administrator-com-object-model.md) | <span data-ttu-id="c7c8e-116">以標準使用者身分執行的應用程式會藉由建立提高許可權的 [元件物件模型](/windows/desktop/com/component-object-model--com--portal) 物件，執行需要系統管理員許可權的作業。</span><span class="sxs-lookup"><span data-stu-id="c7c8e-116">An application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> |



 

 

 
