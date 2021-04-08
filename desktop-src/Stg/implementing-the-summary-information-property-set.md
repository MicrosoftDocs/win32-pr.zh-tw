---
title: 執行摘要資訊屬性集
description: 針對結構化儲存體執行摘要資訊屬性集時，有下列指導方針。
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- 執行摘要資訊屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671067"
---
# <a name="implementing-the-summary-information-property-set"></a><span data-ttu-id="c7978-104">執行摘要資訊屬性集</span><span class="sxs-lookup"><span data-stu-id="c7978-104">Implementing the Summary Information Property Set</span></span>

<span data-ttu-id="c7978-105">針對結構化儲存體執行摘要資訊屬性集時，有下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="c7978-105">There are guidelines to follow when implementing a summary information property set for Structured Storage.</span></span>

<span data-ttu-id="c7978-106">以下是執行 [摘要資訊屬性集](the-summary-information-property-set.md)的指導方針：</span><span class="sxs-lookup"><span data-stu-id="c7978-106">The following are the guidelines for implementing [The Summary Information Property Set](the-summary-information-property-set.md):</span></span>

-   <span data-ttu-id="c7978-107">**PID \_範本** 指的是包含格式和樣式資訊的外部檔。</span><span class="sxs-lookup"><span data-stu-id="c7978-107">**PID\_TEMPLATE** refers to an external document containing format and style information.</span></span> <span data-ttu-id="c7978-108">範本所在的處理常式是由實作為定義。</span><span class="sxs-lookup"><span data-stu-id="c7978-108">The process by which the template is located is implementation-defined.</span></span>
-   <span data-ttu-id="c7978-109">**PID \_LASTAUTHOR** 是應用程式儲存在使用者資訊中的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7978-109">**PID\_LASTAUTHOR** is the name stored in User Information by the application.</span></span> <span data-ttu-id="c7978-110">例如，Mary 在電腦上建立一份檔，並將它提供給 John，然後修改並儲存它。</span><span class="sxs-lookup"><span data-stu-id="c7978-110">For example, Mary creates a document on her computer and gives it to John, who then modifies and saves it.</span></span> <span data-ttu-id="c7978-111">Mary 是作者，John 是最後一個儲存的值。</span><span class="sxs-lookup"><span data-stu-id="c7978-111">Mary is the author, John is the last saved by value.</span></span>
-   <span data-ttu-id="c7978-112">**PID \_REVNUMBER** 是在這份檔上呼叫檔案/儲存命令的次數。</span><span class="sxs-lookup"><span data-stu-id="c7978-112">**PID\_REVNUMBER** is the number of times the File/Save command has been called on this document.</span></span>
-   <span data-ttu-id="c7978-113">每個日期/時間值都必須以全球協調時間儲存 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="c7978-113">Each of the date/time values must be stored in Universal Coordinated Time (UTC).</span></span>
-   <span data-ttu-id="c7978-114">**PID \_建立 \_ DTM** 是唯讀屬性;這個屬性應該在建立檔時設定，但之後不應變更。</span><span class="sxs-lookup"><span data-stu-id="c7978-114">**PID\_CREATE\_DTM** is a read-only property; this property should be set when a document is created, but should not be subsequently changed.</span></span>
-   <span data-ttu-id="c7978-115">針對 **PID \_ 縮圖**，應用程式應該以 **CF \_ .dib** 或 **cf \_ METAFILEPICT** 格式儲存資料。</span><span class="sxs-lookup"><span data-stu-id="c7978-115">For **PID\_THUMBNAIL**, applications should store data in **CF\_DIB** or **CF\_METAFILEPICT** format.</span></span> <span data-ttu-id="c7978-116">**CF \_** 建議使用 METAFILEPICT。</span><span class="sxs-lookup"><span data-stu-id="c7978-116">**CF\_METAFILEPICT** is recommended.</span></span>
-   <span data-ttu-id="c7978-117">**PID \_安全性** 是建議的檔安全性層級。</span><span class="sxs-lookup"><span data-stu-id="c7978-117">**PID\_SECURITY** is the suggested security level for the document.</span></span> <span data-ttu-id="c7978-118">藉由記下檔的安全性層級，檔的建立者以外的應用程式就可以將其使用者介面調整為屬性。</span><span class="sxs-lookup"><span data-stu-id="c7978-118">By noting the security level on the document, an application other than the originator of the document can adjust its user interface to the properties.</span></span> <span data-ttu-id="c7978-119">應用程式不應該顯示任何有關受密碼保護之檔的資訊，或是啟用 Read-Only 或鎖定註釋檔的強制修改。</span><span class="sxs-lookup"><span data-stu-id="c7978-119">An application should not display any information about a password-protected document or enable modifications to enforced Read-Only or Locked-for-Annotations documents.</span></span> <span data-ttu-id="c7978-120">如果使用者嘗試修改屬性，應用程式應該向使用者警告 Read-Only 建議的狀態。</span><span class="sxs-lookup"><span data-stu-id="c7978-120">If the user attempts to modify properties, the application should warn the user about the Read-Only Recommended status.</span></span>



| <span data-ttu-id="c7978-121">安全性層級</span><span class="sxs-lookup"><span data-stu-id="c7978-121">Security level</span></span>         | <span data-ttu-id="c7978-122">值</span><span class="sxs-lookup"><span data-stu-id="c7978-122">Value</span></span> |
|------------------------|-------|
| <span data-ttu-id="c7978-123">無</span><span class="sxs-lookup"><span data-stu-id="c7978-123">None</span></span>                   | <span data-ttu-id="c7978-124">0</span><span class="sxs-lookup"><span data-stu-id="c7978-124">0</span></span>     |
| <span data-ttu-id="c7978-125">密碼保護</span><span class="sxs-lookup"><span data-stu-id="c7978-125">Password protected</span></span>     | <span data-ttu-id="c7978-126">1</span><span class="sxs-lookup"><span data-stu-id="c7978-126">1</span></span>     |
| <span data-ttu-id="c7978-127">建議使用唯讀</span><span class="sxs-lookup"><span data-stu-id="c7978-127">Read-only recommended</span></span>  | <span data-ttu-id="c7978-128">2</span><span class="sxs-lookup"><span data-stu-id="c7978-128">2</span></span>     |
| <span data-ttu-id="c7978-129">強制唯讀</span><span class="sxs-lookup"><span data-stu-id="c7978-129">Read-only enforced</span></span>     | <span data-ttu-id="c7978-130">4</span><span class="sxs-lookup"><span data-stu-id="c7978-130">4</span></span>     |
| <span data-ttu-id="c7978-131">鎖定批註</span><span class="sxs-lookup"><span data-stu-id="c7978-131">Locked for annotations</span></span> | <span data-ttu-id="c7978-132">8</span><span class="sxs-lookup"><span data-stu-id="c7978-132">8</span></span>     |



 

 

 




