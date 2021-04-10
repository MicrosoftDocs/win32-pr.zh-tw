---
description: 磁碟區陰影複製服務 (VSS) 提供系統基礎結構，以便在 Windows 系統上執行 VSS 應用程式。
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: 磁碟區陰影複製服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690479"
---
# <a name="the-volume-shadow-copy-service"></a><span data-ttu-id="803be-103">磁碟區陰影複製服務</span><span class="sxs-lookup"><span data-stu-id="803be-103">The Volume Shadow Copy Service</span></span>

<span data-ttu-id="803be-104">磁碟區陰影複製服務 (VSS) 提供系統基礎結構，以便在 Windows 系統上執行 VSS 應用程式。</span><span class="sxs-lookup"><span data-stu-id="803be-104">The Volume Shadow Copy Service (VSS) provides the system infrastructure for running VSS applications on Windows-based systems.</span></span>

<span data-ttu-id="803be-105">雖然對使用者和開發人員來說大多是透明的，但 VSS 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="803be-105">Though largely transparent to user and developer, VSS does the following:</span></span>

-   <span data-ttu-id="803be-106">在建立和使用陰影複製時，協調提供者、寫入器和要求者的活動</span><span class="sxs-lookup"><span data-stu-id="803be-106">Coordinates activities of providers, writers, and requesters in the creation and use of shadow copies</span></span>
-   <span data-ttu-id="803be-107">提供預設系統提供者</span><span class="sxs-lookup"><span data-stu-id="803be-107">Furnishes the default system provider</span></span>
-   <span data-ttu-id="803be-108">實行任何提供者所需的低層級驅動程式功能</span><span class="sxs-lookup"><span data-stu-id="803be-108">Implements low-level driver functionality necessary for any provider to work</span></span>

<span data-ttu-id="803be-109">VSS 服務會視需要啟動；因此，若要讓 VSS 作業成功，必須啟用此服務。</span><span class="sxs-lookup"><span data-stu-id="803be-109">The VSS service starts on demand; therefore, for VSS operations to be successful, this service must be enabled.</span></span>

 

 



