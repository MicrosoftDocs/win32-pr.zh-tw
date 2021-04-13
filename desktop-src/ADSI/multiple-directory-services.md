---
title: 多個目錄服務
description: 在分散式運算環境內工作的一項挑戰，就是識別和尋找資源（例如使用者、群組、列印佇列和檔）。
ms.assetid: 66929290-b830-4768-a2ae-604d1a9de5c4
ms.tgt_platform: multiple
keywords:
- 多個目錄服務 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2e174fc1b07564f1cca6c12093a289a0c865a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300084"
---
# <a name="multiple-directory-services"></a><span data-ttu-id="8dbf5-104">多個目錄服務</span><span class="sxs-lookup"><span data-stu-id="8dbf5-104">Multiple Directory Services</span></span>

<span data-ttu-id="8dbf5-105">在分散式運算環境內工作的一項挑戰，就是識別和尋找資源（例如使用者、群組、列印佇列和檔）。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-105">One challenge of working within a distributed computing environment is identifying and locating resources such as users, groups, print queues, and documents.</span></span> <span data-ttu-id="8dbf5-106">目錄服務是分散式運算環境的一部分，可讓您找出並識別系統中可用的使用者和資源。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-106">A directory service is the part of a distributed computing environment that provides a way to locate and identify the users and resources available in the system.</span></span> <span data-ttu-id="8dbf5-107">目錄服務就像是電話目錄。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-107">A directory service is like a phone directory.</span></span> <span data-ttu-id="8dbf5-108">針對個人或資源的名稱，它會提供存取該人員或資源所需的資料。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-108">Given a name for a person or a resource, it provides the data necessary to access that person or resource.</span></span> <span data-ttu-id="8dbf5-109">您不需要從系結資料開始，就可以存取網路上的資源。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-109">You do not have to start with binding data to access a resource on the network.</span></span>

<span data-ttu-id="8dbf5-110">大部分的企業都已有許多不同的目錄。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-110">Most enterprises already have many different directories in place.</span></span> <span data-ttu-id="8dbf5-111">例如，網路作業系統、電子郵件系統和「元件」產品都有自己的目錄。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-111">For example, network operating systems, electronic mail systems, and "groupware" products all have their own directories.</span></span> <span data-ttu-id="8dbf5-112">當單一企業部署多個目錄時，會發生許多問題。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-112">Many issues arise when a single enterprise deploys multiple directories.</span></span> <span data-ttu-id="8dbf5-113">這些問題包括可用性、資料一致性、開發成本和支援成本，還有其他問題。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-113">These issues include usability, data consistency, development cost, and support cost, among others.</span></span>

<span data-ttu-id="8dbf5-114">這些問題是在 ADSI 中解決，因為提供了單一、一致、開放的介面集，可用來管理和使用具有 ADSI 提供者的任何目錄服務。</span><span class="sxs-lookup"><span data-stu-id="8dbf5-114">These issues are addressed in ADSI, in that there is provided a single, consistent, open set of interfaces that can be used for managing and using any directory service that has an ADSI provider.</span></span>

 

 




