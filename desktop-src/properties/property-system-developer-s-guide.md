---
description: 瞭解 Windows 屬性系統內自訂屬性和屬性處理常式的開發案例。
ms.assetid: 3281736b-f9ea-4699-a128-3bce6810126e
title: 屬性系統開發人員指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a26044d0d457d4ba24b8c9a18555885c12a571
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988923"
---
# <a name="property-system-developers-guide"></a><span data-ttu-id="0c085-103">屬性系統開發人員指南</span><span class="sxs-lookup"><span data-stu-id="0c085-103">Property System Developer's Guide</span></span>

<span data-ttu-id="0c085-104">在 Windows Vista 和更新版本中，中繼資料成為組織專案（例如檔案、電子郵件或連絡人）之方法的核心。</span><span class="sxs-lookup"><span data-stu-id="0c085-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="0c085-105">為了讓系統能夠根據其中繼資料來搜尋專案，以及使用者可以讀取或寫入該中繼資料的位置，Windows Vista 引進了新的屬性系統。</span><span class="sxs-lookup"><span data-stu-id="0c085-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="0c085-106">這個系統中的中繼資料是由一組可擴充的屬性來表示。</span><span class="sxs-lookup"><span data-stu-id="0c085-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="0c085-107">隨著 Windows Vista 中的內容的推出，將相片、音樂、檔、郵件、連絡人和檔案等專案的細節抽象化， (Isv) 現在如果沒有任何現有的屬性符合需求，就可以將自己的屬性引入平臺。</span><span class="sxs-lookup"><span data-stu-id="0c085-107">With the introduction of properties in Windows Vista that abstracted the specifics of items such as photos, music, documents, messages, contacts, and files, Independent software vendors (ISVs) can now introduce their own properties to the platform if no existing property meets their needs.</span></span>

<span data-ttu-id="0c085-108">本節說明 Windows 屬性系統內的下列開發案例：</span><span class="sxs-lookup"><span data-stu-id="0c085-108">This section describes the following development scenarios within the Windows Property System:</span></span>

-   [<span data-ttu-id="0c085-109">建立自訂屬性</span><span class="sxs-lookup"><span data-stu-id="0c085-109">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
-   [<span data-ttu-id="0c085-110">執行屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="0c085-110">Implementing Property Handlers</span></span>](./building-property-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="0c085-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c085-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c085-112">屬性系統概觀</span><span class="sxs-lookup"><span data-stu-id="0c085-112">Property System Overview</span></span>](property-system-overview.md)
</dt> <dt>

[<span data-ttu-id="0c085-113">屬性系統參考</span><span class="sxs-lookup"><span data-stu-id="0c085-113">Property System Reference</span></span>](property-system-reference.md)
</dt> <dt>

[<span data-ttu-id="0c085-114">屬性系統程式碼範例</span><span class="sxs-lookup"><span data-stu-id="0c085-114">Property System Code Samples</span></span>](property-system-code-samples.md)
</dt> </dl>

 

 
