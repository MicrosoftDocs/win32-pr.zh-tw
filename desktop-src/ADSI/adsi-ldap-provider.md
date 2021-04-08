---
title: ADSI LDAP 提供者
description: ADSI LDAP 提供者會執行一組支援各種 ADSI 介面的 ADSI 物件。 若要存取 LDAP 提供者，請使用 LDAP ADsPath 系結至任何 ADSI LDAP 物件。
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- ADSI LDAP 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839244"
---
# <a name="adsi-ldap-provider"></a><span data-ttu-id="a9020-105">ADSI LDAP 提供者</span><span class="sxs-lookup"><span data-stu-id="a9020-105">ADSI LDAP Provider</span></span>

<span data-ttu-id="a9020-106">ADSI LDAP 提供者會執行一組支援各種 ADSI 介面的 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="a9020-106">The ADSI LDAP Provider implements a set of ADSI objects that support various ADSI interfaces.</span></span> <span data-ttu-id="a9020-107">若要存取 LDAP 提供者，請使用 LDAP ADsPath 系結至任何 ADSI LDAP 物件。</span><span class="sxs-lookup"><span data-stu-id="a9020-107">To access the LDAP provider, bind to any of the ADSI LDAP objects, using the LDAP ADsPath.</span></span>

<span data-ttu-id="a9020-108">您必須在用戶端電腦上安裝 Adsldp.dll、Adsldpc.dll、Adsmsext.dll 和 Activeds.dll，才能與提供者搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a9020-108">You must have Adsldp.dll, Adsldpc.dll, Adsmsext.dll, and Activeds.dll installed on your client computer to work with the provider.</span></span>

> [!Note]  
> <span data-ttu-id="a9020-109">預設的 ADSI LDAP 提供者無法假設為完全安全線程。</span><span class="sxs-lookup"><span data-stu-id="a9020-109">The default ADSI LDAP provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="a9020-110">多執行緒應用程式的寫入器應該透過適當的同步處理物件（例如，信號、mutex、重要區段等等）來適當地協調執行緒之間的存取。</span><span class="sxs-lookup"><span data-stu-id="a9020-110">Writers of multithreaded applications should properly coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




