---
description: 使用傳統安裝技術時，必須結束應用程式並重新執行安裝程式，才能執行安裝工作。
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: 隨選安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f25c83135a0497d09aa0a7800a1272105d0db1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193110"
---
# <a name="installation-on-demand"></a><span data-ttu-id="94c45-103">隨選安裝</span><span class="sxs-lookup"><span data-stu-id="94c45-103">Installation-On-Demand</span></span>

<span data-ttu-id="94c45-104">使用傳統安裝技術時，必須結束應用程式並重新執行安裝程式，才能執行安裝工作。</span><span class="sxs-lookup"><span data-stu-id="94c45-104">With traditional installation technology, it is necessary to exit an application and rerun setup to perform an installation task.</span></span> <span data-ttu-id="94c45-105">當使用者想要在第一次執行安裝程式期間未選擇的功能或產品時，通常就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="94c45-105">This commonly occurred when a user wanted a feature or product not chosen during the first run of setup.</span></span> <span data-ttu-id="94c45-106">這通常會讓產品設定的程式效率不佳，因為它需要使用者先預期需要的功能，才能使用該產品。</span><span class="sxs-lookup"><span data-stu-id="94c45-106">This often made the process of product configuration inefficient because it required the user to anticipate the functionality required before they ever used the product.</span></span>

<span data-ttu-id="94c45-107">隨選安裝讓您能夠在沒有檔案本身的情況下，為使用者和應用程式提供功能。</span><span class="sxs-lookup"><span data-stu-id="94c45-107">Installation-on-demand makes it possible to offer functionality to users and applications in the absence of the files themselves.</span></span> <span data-ttu-id="94c45-108">這個概念稱為「通告」。</span><span class="sxs-lookup"><span data-stu-id="94c45-108">This notion is known as advertisement.</span></span> <span data-ttu-id="94c45-109">Windows Installer 具有廣告功能的功能，並可讓您視需要進行應用程式功能或整個產品的安裝。</span><span class="sxs-lookup"><span data-stu-id="94c45-109">The Windows Installer has the capability of advertising functionality and to make installation-on-demand of application features or entire products possible.</span></span> <span data-ttu-id="94c45-110">當使用者或應用程式啟用已公告的功能或產品時，安裝程式會繼續安裝所需的元件。</span><span class="sxs-lookup"><span data-stu-id="94c45-110">When a user or application activates an advertised feature or product, the installer proceeds with installation of the needed components.</span></span> <span data-ttu-id="94c45-111">這會縮短設定程式，因為可以存取額外的功能，而不需要結束再重新執行另一個安裝程式。</span><span class="sxs-lookup"><span data-stu-id="94c45-111">This shortens the configuration process because additional functionality can be accessed without having to exit and rerun another setup procedure.</span></span>

<span data-ttu-id="94c45-112">當產品使用安裝程式時，使用者可以在安裝時選擇要安裝的功能或應用程式，以及要通告的應用程式。</span><span class="sxs-lookup"><span data-stu-id="94c45-112">When a product uses the installer, a user can choose at setup time which features or applications to install and which to advertise.</span></span> <span data-ttu-id="94c45-113">然後，如果在執行應用程式時，使用者要求尚未安裝的已公告功能，應用程式就會呼叫安裝程式，以制定及時的功能層級安裝所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="94c45-113">Then if while running an application the user requests an advertised feature that has not yet been installed, the application calls the installer to enact a just-in-time feature level installation of the necessary files.</span></span> <span data-ttu-id="94c45-114">如果使用者啟用尚未安裝的已公告產品，作業系統會呼叫安裝程式來制定及時的產品層級安裝。</span><span class="sxs-lookup"><span data-stu-id="94c45-114">If the user activates an advertised product that has not yet been installed, the operating system calls the installer to enact a just-in-time product level installation.</span></span>

<span data-ttu-id="94c45-115">[公告](advertisement.md) 和隨選安裝也可以讓系統管理員針對不同的使用者群組，將應用程式指定為必要或選擇性，以協助進行系統管理。</span><span class="sxs-lookup"><span data-stu-id="94c45-115">[Advertisement](advertisement.md) and installation-on-demand can also facilitate system management by enabling administrators to designate applications as required or optional for different groups of users.</span></span> <span data-ttu-id="94c45-116">有兩種類型的廣告稱為「指派」和「發佈」。</span><span class="sxs-lookup"><span data-stu-id="94c45-116">There are two types of advertising known as "assigning" and "publishing."</span></span> <span data-ttu-id="94c45-117">如果系統管理員將應用程式指派給群組，這些使用者就可以視需要安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="94c45-117">If an administrator assigns an application to a group, then these users can install the application on-demand.</span></span> <span data-ttu-id="94c45-118">但是，如果系統管理員將應用程式發佈至群組，則不會對這些使用者顯示任何進入點，而且只有當另一個應用程式啟動已發佈的應用程式時，才會啟用隨選安裝。</span><span class="sxs-lookup"><span data-stu-id="94c45-118">If, however, the administrator publishes the application to the group, no entry points appear to these users and installation-on-demand is only activated if another application activates the published application.</span></span>

 

 



