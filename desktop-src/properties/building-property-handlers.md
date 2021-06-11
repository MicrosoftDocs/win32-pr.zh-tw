---
description: 瞭解如何建立可在檔案資料流程中讀取和寫入屬性的屬性處理常式。 每個處理常式都與指定的檔案類型相關聯。
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: 執行屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf37ae37e43ce14cf69bec44e7f210b32373d38e
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989263"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="febd8-104">執行屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="febd8-104">Implementing Property Handlers</span></span>

<span data-ttu-id="febd8-105">在 Windows Vista 和更新版本中，中繼資料成為組織專案（例如檔案、電子郵件或連絡人）之方法的核心。</span><span class="sxs-lookup"><span data-stu-id="febd8-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="febd8-106">為了讓系統能夠根據其中繼資料來搜尋專案，以及使用者可以讀取或寫入該中繼資料的位置，Windows Vista 引進了新的屬性系統。</span><span class="sxs-lookup"><span data-stu-id="febd8-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="febd8-107">這個系統中的中繼資料是由一組可擴充的屬性來表示。</span><span class="sxs-lookup"><span data-stu-id="febd8-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="febd8-108">在這組主題中，我們會說明如何建立可在檔案資料流程中讀取和寫入屬性的處理常式。</span><span class="sxs-lookup"><span data-stu-id="febd8-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="febd8-109">這些處理常式稱為「屬性處理常式」（property），而每個處理常式都與指定的檔案類型相關聯，並以副檔名來識別。</span><span class="sxs-lookup"><span data-stu-id="febd8-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="febd8-110">下列主題討論定義屬性和屬性處理常式所需的需求和策略。</span><span class="sxs-lookup"><span data-stu-id="febd8-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="febd8-111">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="febd8-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="febd8-112">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="febd8-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="febd8-113">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="febd8-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="febd8-114">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="febd8-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="febd8-115">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="febd8-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="febd8-116">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="febd8-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="febd8-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="febd8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="febd8-118">建立自訂屬性</span><span class="sxs-lookup"><span data-stu-id="febd8-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="febd8-119">屬性描述架構</span><span class="sxs-lookup"><span data-stu-id="febd8-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
