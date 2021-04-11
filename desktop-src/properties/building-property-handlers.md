---
description: 在 Windows Vista 和更新版本中，中繼資料成為組織專案（例如檔案、電子郵件或連絡人）之方法的核心。
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: 執行屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193761"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="1be2e-103">執行屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="1be2e-103">Implementing Property Handlers</span></span>

<span data-ttu-id="1be2e-104">在 Windows Vista 和更新版本中，中繼資料成為組織專案（例如檔案、電子郵件或連絡人）之方法的核心。</span><span class="sxs-lookup"><span data-stu-id="1be2e-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="1be2e-105">為了讓系統能夠根據其中繼資料來搜尋專案，以及使用者可以讀取或寫入該中繼資料的位置，Windows Vista 引進了新的屬性系統。</span><span class="sxs-lookup"><span data-stu-id="1be2e-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="1be2e-106">這個系統中的中繼資料是由一組可擴充的屬性來表示。</span><span class="sxs-lookup"><span data-stu-id="1be2e-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="1be2e-107">在這組主題中，我們會說明如何建立可在檔案資料流程中讀取和寫入屬性的處理常式。</span><span class="sxs-lookup"><span data-stu-id="1be2e-107">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="1be2e-108">這些處理常式稱為「屬性處理常式」（property），而每個處理常式都與指定的檔案類型相關聯，並以副檔名來識別。</span><span class="sxs-lookup"><span data-stu-id="1be2e-108">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="1be2e-109">下列主題討論定義屬性和屬性處理常式所需的需求和策略。</span><span class="sxs-lookup"><span data-stu-id="1be2e-109">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="1be2e-110">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="1be2e-110">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="1be2e-111">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="1be2e-111">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="1be2e-112">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="1be2e-112">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="1be2e-113">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="1be2e-113">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="1be2e-114">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="1be2e-114">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="1be2e-115">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="1be2e-115">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="1be2e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1be2e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1be2e-117">建立自訂屬性</span><span class="sxs-lookup"><span data-stu-id="1be2e-117">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="1be2e-118">屬性描述架構</span><span class="sxs-lookup"><span data-stu-id="1be2e-118">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
