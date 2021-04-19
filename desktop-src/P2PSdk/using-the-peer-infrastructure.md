---
description: 本節討論使用對等基礎結構開發應用程式的實際考慮，以及更有效率地使用 Api 的特定技術。
ms.assetid: 5ce0f8a6-ab61-4091-809f-2e4a990f4886
title: 使用對等基礎結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6cbcaab4044aa1f0b3e3ca017c824bf304f634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983642"
---
# <a name="using-the-peer-infrastructure"></a><span data-ttu-id="19b04-103">使用對等基礎結構</span><span class="sxs-lookup"><span data-stu-id="19b04-103">Using the Peer Infrastructure</span></span>

<span data-ttu-id="19b04-104">本節討論使用對等基礎結構開發應用程式的實際考慮，以及更有效率地使用 Api 的特定技術。</span><span class="sxs-lookup"><span data-stu-id="19b04-104">This section discusses practical considerations for developing applications with the Peer infrastructure, as well as specific techniques to use the APIs more efficiently.</span></span>

<span data-ttu-id="19b04-105">下列主題會識別使用對等基礎結構開發應用程式之一般工作的解決方案。</span><span class="sxs-lookup"><span data-stu-id="19b04-105">The following topics identify solutions to common tasks for developing applications using the Peer Infrastructure.</span></span>



| <span data-ttu-id="19b04-106">主題</span><span class="sxs-lookup"><span data-stu-id="19b04-106">Topic</span></span>                                                                                                        | <span data-ttu-id="19b04-107">描述</span><span class="sxs-lookup"><span data-stu-id="19b04-107">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19b04-108">安裝對等基礎結構</span><span class="sxs-lookup"><span data-stu-id="19b04-108">Installing the Peer Infrastructure</span></span>](installing-the-peer-infrastructure.md)                                 | <span data-ttu-id="19b04-109">識別如何在 Windows XP 中安裝對等基礎結構。</span><span class="sxs-lookup"><span data-stu-id="19b04-109">Identifies how to install the Peer Infrastructure in Windows XP.</span></span>                                                        |
| [<span data-ttu-id="19b04-110">程式設計考量</span><span class="sxs-lookup"><span data-stu-id="19b04-110">Programming Considerations</span></span>](programming-considerations.md)                                                 | <span data-ttu-id="19b04-111">識別使用對等基礎結構開發應用程式時的重要程式設計考慮。</span><span class="sxs-lookup"><span data-stu-id="19b04-111">Identifies important programming considerations for developing applications using the Peer Infrastructure.</span></span>              |
| [<span data-ttu-id="19b04-112">安全性考量</span><span class="sxs-lookup"><span data-stu-id="19b04-112">Security Considerations</span></span>](security-considerations.md)                                                       | <span data-ttu-id="19b04-113">識別使用對等基礎結構開發應用程式時的重要安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="19b04-113">Identifies important security considerations for developing applications using the Peer Infrastructure.</span></span>                 |
| [<span data-ttu-id="19b04-114">資料庫匯入和匯出</span><span class="sxs-lookup"><span data-stu-id="19b04-114">Database Import and Export</span></span>](database-import-and-export.md)                                                 | <span data-ttu-id="19b04-115">識別如何匯入和匯出記錄資料庫。</span><span class="sxs-lookup"><span data-stu-id="19b04-115">Identifies how to import and export record databases.</span></span>                                                                   |
| [<span data-ttu-id="19b04-116">直接連接</span><span class="sxs-lookup"><span data-stu-id="19b04-116">Direct Connections</span></span>](direct-connections.md)                                                                 | <span data-ttu-id="19b04-117">識別如何在對等圖形和群組 Api 之間，使用和之間的直接連接。</span><span class="sxs-lookup"><span data-stu-id="19b04-117">Identifies how to work with direct connections between and among peers from within the Peer Graphing and Grouping APIs.</span></span> |
| [<span data-ttu-id="19b04-118">列舉</span><span class="sxs-lookup"><span data-stu-id="19b04-118">Enumerations</span></span>](enumerations.md)                                                                             | <span data-ttu-id="19b04-119">識別如何使用對等基礎結構使用的列舉函數。</span><span class="sxs-lookup"><span data-stu-id="19b04-119">Identifies how to work with the enumeration functions that the Peer Infrastructure uses.</span></span>                                |
| [<span data-ttu-id="19b04-120">釋放對等資料</span><span class="sxs-lookup"><span data-stu-id="19b04-120">Freeing Peer Data</span></span>](freeing-peer-data.md)                                                                   | <span data-ttu-id="19b04-121">識別如何釋放傳回的資料一般對等基礎結構函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="19b04-121">Identifies how to release data common Peer Infrastructure function calls returned.</span></span>                                      |
| [<span data-ttu-id="19b04-122">事件基礎結構</span><span class="sxs-lookup"><span data-stu-id="19b04-122">Events Infrastructure</span></span>](peer-events-infrastructure.md)                                                      | <span data-ttu-id="19b04-123">識別如何使用對等事件，以及解讀對等圖形和圖形 Api 定義的事件。</span><span class="sxs-lookup"><span data-stu-id="19b04-123">Identifies how to work with the peer events, and interpret the events that the Peer Graphing and Graphing APIs define.</span></span>  |
| [<span data-ttu-id="19b04-124">身分識別和群組設定匯入和匯出</span><span class="sxs-lookup"><span data-stu-id="19b04-124">Identity and Group Configuration Import and Export</span></span>](identity-and-group-configuration-import-and-export.md) | <span data-ttu-id="19b04-125">識別如何匯入和匯出對等身分識別和群組身分識別設定。</span><span class="sxs-lookup"><span data-stu-id="19b04-125">Identifies how to import and export peer identity and group identity configurations.</span></span>                                    |
| [<span data-ttu-id="19b04-126">記錄</span><span class="sxs-lookup"><span data-stu-id="19b04-126">Records</span></span>](records.md)                                                                                       | <span data-ttu-id="19b04-127">識別如何使用對等記錄和記錄資料庫。</span><span class="sxs-lookup"><span data-stu-id="19b04-127">Identifies how to work with peer records and the record database.</span></span>                                                       |



 

 

 



