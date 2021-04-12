---
title: 將 ADSI 介面對應到網路管理功能
description: Active Directory 服務介面 (ADSI) 是一組 COM 介面，可用來從不同的網路提供者存取目錄服務的功能。
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ec1a1055d3d016bf8b7b1bd3f357810b7ddd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316432"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a><span data-ttu-id="71a34-103">將 ADSI 介面對應到網路管理功能</span><span class="sxs-lookup"><span data-stu-id="71a34-103">Mapping ADSI Interfaces to the Network Management Functions</span></span>

<span data-ttu-id="71a34-104">Active Directory 服務介面 (ADSI) 是一組 COM 介面，可用來從不同的網路提供者存取目錄服務的功能。</span><span class="sxs-lookup"><span data-stu-id="71a34-104">The Active Directory Service Interfaces (ADSI) are a set of COM interfaces used to access the capabilities of directory services from different network providers.</span></span> <span data-ttu-id="71a34-105">ADSI 提供一組目錄服務介面，用來管理分散式運算環境中的網路資源。</span><span class="sxs-lookup"><span data-stu-id="71a34-105">ADSI presents a single set of directory service interfaces for managing network resources in a distributed computing environment.</span></span>

<span data-ttu-id="71a34-106">如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定的 ADSI 介面方法，以取得您可以藉由呼叫特定網路管理功能來達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="71a34-106">If you are programming for Active Directory, you may be able to call certain ADSI interface methods to achieve the same functionality you can achieve by calling certain network management functions.</span></span>

<span data-ttu-id="71a34-107">下表列出網路管理功能和函數群組，以及函式所對應的 ADSI 介面。</span><span class="sxs-lookup"><span data-stu-id="71a34-107">The following table lists network management functions and function groups, and the ADSI interfaces to which the functions map.</span></span>



| <span data-ttu-id="71a34-108">函式</span><span class="sxs-lookup"><span data-stu-id="71a34-108">Functions</span></span>                                                                  | <span data-ttu-id="71a34-109">介面</span><span class="sxs-lookup"><span data-stu-id="71a34-109">Interfaces</span></span>                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a34-110">[**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)、 [ **NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo)</span><span class="sxs-lookup"><span data-stu-id="71a34-110">[**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum), [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo)</span></span> | <span data-ttu-id="71a34-111">[**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource)、 [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)</span><span class="sxs-lookup"><span data-stu-id="71a34-111">[**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource), [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)</span></span> |
| <span data-ttu-id="71a34-112">[NetGroup](group-functions.md)\*</span><span class="sxs-lookup"><span data-stu-id="71a34-112">[NetGroup](group-functions.md)\*</span></span>                                          | [<span data-ttu-id="71a34-113">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="71a34-113">**IADsGroup**</span></span>](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| <span data-ttu-id="71a34-114">[NetLocalGroup](local-group-functions.md)\*</span><span class="sxs-lookup"><span data-stu-id="71a34-114">[NetLocalGroup](local-group-functions.md)\*</span></span>                               | [<span data-ttu-id="71a34-115">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="71a34-115">**IADsGroup**</span></span>](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| <span data-ttu-id="71a34-116">[NetServer](server-functions.md)\*</span><span class="sxs-lookup"><span data-stu-id="71a34-116">[NetServer](server-functions.md)\*</span></span>                                        | [<span data-ttu-id="71a34-117">**IADsComputer**</span><span class="sxs-lookup"><span data-stu-id="71a34-117">**IADsComputer**</span></span>](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| <span data-ttu-id="71a34-118">[NetSession](session-functions.md)\*</span><span class="sxs-lookup"><span data-stu-id="71a34-118">[NetSession](session-functions.md)\*</span></span>                                      | <span data-ttu-id="71a34-119">[**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession)、 [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)</span><span class="sxs-lookup"><span data-stu-id="71a34-119">[**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession), [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)</span></span>   |
| <span data-ttu-id="71a34-120">[NetShare](share-functions.md)\*</span><span class="sxs-lookup"><span data-stu-id="71a34-120">[NetShare](share-functions.md)\*</span></span>                                          | [<span data-ttu-id="71a34-121">**IADsFileShare**</span><span class="sxs-lookup"><span data-stu-id="71a34-121">**IADsFileShare**</span></span>](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| <span data-ttu-id="71a34-122">[NetUser](user-functions.md)\*</span><span class="sxs-lookup"><span data-stu-id="71a34-122">[NetUser](user-functions.md)\*</span></span>                                            | <span data-ttu-id="71a34-123">[**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)、 [ **IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)</span><span class="sxs-lookup"><span data-stu-id="71a34-123">[**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)</span></span>                                   |
| <span data-ttu-id="71a34-124">[NetUserModals](user-modal-functions.md)\*</span><span class="sxs-lookup"><span data-stu-id="71a34-124">[NetUserModals](user-modal-functions.md)\*</span></span>                                | [<span data-ttu-id="71a34-125">**IADsDomain**</span><span class="sxs-lookup"><span data-stu-id="71a34-125">**IADsDomain**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

<span data-ttu-id="71a34-126">如需有關目錄服務和使用 ADSI 進行程式設計的詳細資訊，請參閱 [Active Directory 服務介面](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)。</span><span class="sxs-lookup"><span data-stu-id="71a34-126">For more information about directory services and programming with ADSI, see [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).</span></span> <span data-ttu-id="71a34-127">如需 WinNT 提供者可供使用者類別使用之自訂屬性的相關資訊，以及 WinNT 提供者不支援之 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) 介面的屬性方法，請參閱 [ADSI WinNT 提供者](/windows/desktop/ADSI/adsi-winnt-provider)。</span><span class="sxs-lookup"><span data-stu-id="71a34-127">For information about the custom properties the WinNT provider makes available for the User class, and the property methods of the [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) interface the WinNT provider does not support, see [ADSI WinNT Provider](/windows/desktop/ADSI/adsi-winnt-provider).</span></span>

 

 