---
description: 當發生憑證發行之類的作業時，結束模組會接收來自伺服器引擎的通知。
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: 結束模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc0668717c4a7a690cce8a03ff8c140333347b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193895"
---
# <a name="exit-modules"></a><span data-ttu-id="761af-103">結束模組</span><span class="sxs-lookup"><span data-stu-id="761af-103">Exit Modules</span></span>

<span data-ttu-id="761af-104">當發生憑證發行之類的作業時，結束模組會接收來自伺服器引擎的通知。</span><span class="sxs-lookup"><span data-stu-id="761af-104">Exit modules receive notifications from the server engine when operations such as the issuance of a certificate occur.</span></span> <span data-ttu-id="761af-105">Exit 模組會實作為 [*動態連結程式庫*](../secgloss/d-gly.md) ， (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="761af-105">An exit module is implemented as a [*dynamic-link library*](../secgloss/d-gly.md) (DLL).</span></span> <span data-ttu-id="761af-106">結束模組的一般作業是將已完成的憑證發佈到預設的企業憑證授權單位單位結束模組 (指定的位置，例如，將使用者憑證和 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) 發佈到 Active Directory) 。</span><span class="sxs-lookup"><span data-stu-id="761af-106">A typical operation for an exit module is to publish a completed certificate in a specified location (the default enterprise certification authority exit module, for instance, publishes user certificates and [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs) to the Active Directory).</span></span> <span data-ttu-id="761af-107">結束模組可以使用 [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) 介面與憑證服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="761af-107">An exit module can use the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface to communicate with Certificate Services.</span></span> <span data-ttu-id="761af-108">憑證服務會透過直接 COM 呼叫來與結束模組進行通訊，或者，如果模組不支援透過自動化的直接 COM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="761af-108">Certificate Services communicates with an exit module by means of direct COM calls or, if the module does not support direct COM calls, by means of Automation.</span></span>

<span data-ttu-id="761af-109">結束模組可查看現有的憑證屬性和擴充功能，也可能會查看要求屬性和屬性。</span><span class="sxs-lookup"><span data-stu-id="761af-109">An exit module may view existing certificate properties and extensions, and it may also view request attributes and properties.</span></span> <span data-ttu-id="761af-110">但是，exit 模組無法修改任何屬性。</span><span class="sxs-lookup"><span data-stu-id="761af-110">An exit module cannot, however, modify any properties.</span></span>

<span data-ttu-id="761af-111">憑證服務提供預設的結束模組，但您也可以建立自訂的結束模組來符合特殊需求。</span><span class="sxs-lookup"><span data-stu-id="761af-111">Certificate Services provides a default exit module, but you can also create custom exit modules to meet special needs.</span></span> <span data-ttu-id="761af-112">不過，在撰寫自訂結束模組之前，請考慮使用預設的結束模組。</span><span class="sxs-lookup"><span data-stu-id="761af-112">However, before writing a custom exit module, consider using the default exit module.</span></span> <span data-ttu-id="761af-113">此外，對於企業憑證授權單位單位而言，應該一律使用預設的結束模組，即使您可以新增其他自訂的結束模組也是一樣。</span><span class="sxs-lookup"><span data-stu-id="761af-113">Moreover, for an enterprise certification authority, the default exit module should always be used, even though you can add additional, custom exit modules.</span></span> <span data-ttu-id="761af-114">如需詳細資訊，請參閱 [撰寫自訂結束模組](writing-custom-exit-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="761af-114">For more information, see [Writing Custom Exit Modules](writing-custom-exit-modules.md).</span></span>

 

 
