---
description: VSS 安全性問題
ms.assetid: 99dacdbb-9c40-48dd-b5fe-2f13de7af140
title: VSS 安全性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af561b512dd5dbaec954707a813c76391c1ee43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973647"
---
# <a name="vss-security-issues"></a><span data-ttu-id="e060e-103">VSS 安全性問題</span><span class="sxs-lookup"><span data-stu-id="e060e-103">VSS Security Issues</span></span>

<span data-ttu-id="e060e-104">VSS 基礎結構在內部是以 COM 為基礎，因此允許寫入器和要求者進行通訊，需要以 COM 為基礎的安全性。</span><span class="sxs-lookup"><span data-stu-id="e060e-104">The VSS infrastructure is internally based on COM, and therefore allowing writers and requesters to communicate requires COM-based security.</span></span> <span data-ttu-id="e060e-105">COM 安全性提供了 VSS 開發人員應考慮的機制和指導方針：</span><span class="sxs-lookup"><span data-stu-id="e060e-105">COM security provides mechanisms and guidelines that a VSS developer should consider:</span></span>

-   [<span data-ttu-id="e060e-106">寫入器的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="e060e-106">Security Considerations for Writers</span></span>](security-considerations-for-writers.md)
-   [<span data-ttu-id="e060e-107">要求者的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="e060e-107">Security Considerations for Requesters</span></span>](security-considerations-for-requestors.md)

 

 



