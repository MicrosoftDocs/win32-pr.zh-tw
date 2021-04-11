---
description: 對等身分識別管理員 API 可讓您在對等應用程式中建立、列舉和操作對等身分識別。
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: 關於 Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849319"
---
# <a name="about-identity-manager"></a><span data-ttu-id="5527a-103">關於 Identity Manager</span><span class="sxs-lookup"><span data-stu-id="5527a-103">About Identity Manager</span></span>

<span data-ttu-id="5527a-104">對等身分識別管理員 API 可讓您在對等應用程式中建立、列舉和操作對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="5527a-104">The Peer Identity Manager API allows you to create, enumerate, and manipulate peer identities in a peer application.</span></span> <span data-ttu-id="5527a-105">您可以使用使用此 API 所建立的對等身分識別，做為對等群組和對等名稱解析通訊協定的輸入， (PNRP) 命名空間提供者 Api。</span><span class="sxs-lookup"><span data-stu-id="5527a-105">You can use the peer identities created using this API as input for the Peer Grouping and Peer Name Resolution Protocol (PNRP) Namespace Provider APIs.</span></span>

## <a name="peer-identity-manager-best-practices"></a><span data-ttu-id="5527a-106">對等身分識別管理員的最佳作法</span><span class="sxs-lookup"><span data-stu-id="5527a-106">Peer Identity Manager Best Practices</span></span>

<span data-ttu-id="5527a-107">每個使用者都應該有一些可用於對等活動的對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="5527a-107">Each user should have a few peer identities that they can use for the peer activities.</span></span> <span data-ttu-id="5527a-108">例如，使用者可能有兩個對等身分識別可用於工作和休閒。</span><span class="sxs-lookup"><span data-stu-id="5527a-108">For example, a user might have two peer identities for work and leisure.</span></span>

<span data-ttu-id="5527a-109">設計完善的對等應用程式可讓使用者選取要使用的對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="5527a-109">A well-designed peer application allows a user to select a peer identity to use.</span></span> <span data-ttu-id="5527a-110">如果沒有任何現有的對等身分識別適合與應用程式搭配使用，則使用者可以建立新的對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="5527a-110">A user can create a new peer identity if none of the existing peer identities are appropriate to use with an application.</span></span>

<span data-ttu-id="5527a-111">設計完善的對等應用程式也會控制其所建立的身分識別數目。</span><span class="sxs-lookup"><span data-stu-id="5527a-111">A well-designed peer application also controls the number of identities that it creates.</span></span> <span data-ttu-id="5527a-112">如果應用程式建立暫時性對等身分識別，則應用程式必須在不需要身分識別時刪除對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="5527a-112">If an application creates a temporary peer identity, the application must delete the peer identity when the identity is not needed.</span></span> <span data-ttu-id="5527a-113">如果應用程式未執行此維護，對等身分識別管理員可能會在移除某些對等身分識別之前，無法建立對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="5527a-113">If an application does not perform this maintenance, the Peer Identity Manager may not be able to create peer identities until some peer identities are removed.</span></span>

 

 



