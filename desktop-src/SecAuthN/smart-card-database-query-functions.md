---
description: 查詢智慧卡資料庫。 他們可以提供特定使用者提供的智慧卡清單、特定卡片的介面和主要服務提供者、系統定義的讀者群組，以及一組讀者群組內的讀取器。
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: 智慧卡資料庫查詢函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194202"
---
# <a name="smart-card-database-query-functions"></a><span data-ttu-id="c7e43-104">智慧卡資料庫查詢函數</span><span class="sxs-lookup"><span data-stu-id="c7e43-104">Smart Card Database Query Functions</span></span>

<span data-ttu-id="c7e43-105">下列函數會查詢 [*智慧卡資料庫*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c7e43-105">The following functions query the [*smart card database*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c7e43-106">他們可以提供特定使用者提供的智慧卡清單、特定卡片的介面和 [*主要服務提供者*](../secgloss/p-gly.md) 、系統定義的 [*讀者群組*](../secgloss/r-gly.md) ，以及一組讀者 [*群組內的讀取器*](../secgloss/r-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="c7e43-106">They can provide a list of smart cards supplied by a specific user, the interfaces and [*primary service provider*](../secgloss/p-gly.md) of a specific card, the [*reader groups*](../secgloss/r-gly.md) defined for the system, and the [*readers*](../secgloss/r-gly.md) within a set of reader groups.</span></span>

<span data-ttu-id="c7e43-107">當您使用這些函式時，您可以查詢完整的智慧卡資料庫，也可以藉由設定 [*資源管理員內容*](../secgloss/r-gly.md)來縮小搜尋範圍。</span><span class="sxs-lookup"><span data-stu-id="c7e43-107">When you use these functions, you can query the complete smart card database, or you can narrow the search by setting the [*resource manager context*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="c7e43-108">在呼叫查詢函式之前，會先呼叫 [**SCardEstablishCoNtext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) 來設定資源管理員內容。</span><span class="sxs-lookup"><span data-stu-id="c7e43-108">The resource manager context is set by calling [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) before calling a query function.</span></span>

> [!Note]  
> <span data-ttu-id="c7e43-109">如果沒有指定的內容，某些資訊可能仍會因為安全性限制而無法存取。</span><span class="sxs-lookup"><span data-stu-id="c7e43-109">Without a specified context, some information may still be inaccessible due to security restrictions.</span></span>

 



| <span data-ttu-id="c7e43-110">主題</span><span class="sxs-lookup"><span data-stu-id="c7e43-110">Topic</span></span>                                                  | <span data-ttu-id="c7e43-111">描述</span><span class="sxs-lookup"><span data-stu-id="c7e43-111">Description</span></span>                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7e43-112">**SCardGetProviderId**</span><span class="sxs-lookup"><span data-stu-id="c7e43-112">**SCardGetProviderId**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | <span data-ttu-id="c7e43-113">取得指定卡片之 [*主要服務提供者*](../secgloss/p-gly.md) 的識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="c7e43-113">Retrieve the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the given card.</span></span> |
| [<span data-ttu-id="c7e43-114">**SCardListCards**</span><span class="sxs-lookup"><span data-stu-id="c7e43-114">**SCardListCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | <span data-ttu-id="c7e43-115">取得特定使用者先前向系統介紹的卡片清單。</span><span class="sxs-lookup"><span data-stu-id="c7e43-115">Retrieve a list of cards previously introduced to the system by a specific user.</span></span>                                                                                                     |
| [<span data-ttu-id="c7e43-116">**SCardListInterfaces**</span><span class="sxs-lookup"><span data-stu-id="c7e43-116">**SCardListInterfaces**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | <span data-ttu-id="c7e43-117">取得指定卡片所提供介面 (Guid) 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7e43-117">Retrieve the identifiers (GUIDs) of the interfaces supplied by a given card.</span></span>                                                                                                         |
| [<span data-ttu-id="c7e43-118">**SCardListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="c7e43-118">**SCardListReaderGroups**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | <span data-ttu-id="c7e43-119">取出先前引進系統的讀者群組清單。</span><span class="sxs-lookup"><span data-stu-id="c7e43-119">Retrieve a list of reader groups that have previously been introduced to the system.</span></span>                                                                                                 |
| [<span data-ttu-id="c7e43-120">**SCardListReaders**</span><span class="sxs-lookup"><span data-stu-id="c7e43-120">**SCardListReaders**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | <span data-ttu-id="c7e43-121">在一組指定的讀取器群組內取出讀取器清單。</span><span class="sxs-lookup"><span data-stu-id="c7e43-121">Retrieve the list of readers within a set of named reader groups.</span></span>                                                                                                                    |



 

 

 
