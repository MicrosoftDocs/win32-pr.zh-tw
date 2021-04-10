---
title: 複合檔案
description: 雖然您可以執行自己的結構化儲存體物件和介面，但 COM 會提供一個稱為複合檔案的標準實作為。
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183120"
---
# <a name="compound-files"></a><span data-ttu-id="d51d7-103">複合檔案</span><span class="sxs-lookup"><span data-stu-id="d51d7-103">Compound Files</span></span>

<span data-ttu-id="d51d7-104">雖然您可以執行自己的結構化儲存體物件和介面，但 COM 會提供一個稱為複合檔案的標準實作為。</span><span class="sxs-lookup"><span data-stu-id="d51d7-104">Although you can implement your own structured storage objects and interfaces, COM provides a standard implementation called Compound Files.</span></span> <span data-ttu-id="d51d7-105">使用複合檔案可讓您為自己的結構化儲存體執行編寫程式碼，並授數個衍生自訂標準的額外優點。</span><span class="sxs-lookup"><span data-stu-id="d51d7-105">Using Compound Files saves you the work of coding your own implementation of structured storage and confers several additional benefits derived from adhering to a defined standard.</span></span> <span data-ttu-id="d51d7-106">這些優點包括：</span><span class="sxs-lookup"><span data-stu-id="d51d7-106">These benefits include the following:</span></span>

-   <span data-ttu-id="d51d7-107">**檔案系統和平臺獨立性**。</span><span class="sxs-lookup"><span data-stu-id="d51d7-107">**File-system and platform independence**.</span></span> <span data-ttu-id="d51d7-108">由於 COM 的複合檔案執行是在現有的一般檔案系統上執行，因此，儲存在 FAT 檔案系統、NTFS 檔案系統或 Macintosh 檔案系統中的複合檔案可以由使用任何其他檔案系統的應用程式來開啟。</span><span class="sxs-lookup"><span data-stu-id="d51d7-108">Because COM's Compound Files implementation runs on top of existing flat-file systems, compound files stored in the FAT file system, NTFS file system, or Macintosh file systems can be opened by applications using any one of the other file systems.</span></span>
-   <span data-ttu-id="d51d7-109">可 **搜尋。**</span><span class="sxs-lookup"><span data-stu-id="d51d7-109">**Searchable**.</span></span> <span data-ttu-id="d51d7-110">由於複合檔案中的個別物件會儲存為標準格式，而且可以使用標準的 COM 介面和 Api 來存取，因此使用這些介面和 Api 的任何瀏覽器公用程式都可以列出檔案中的物件，即使指定物件內的資料可能採用專屬格式也一樣。</span><span class="sxs-lookup"><span data-stu-id="d51d7-110">Because the separate objects in a compound file are saved in a standard format and can be accessed using standard COM interfaces and APIs, any browser utility using these interfaces and APIs can list the objects in the file, even though data within a given object may be in a proprietary format.</span></span>
-   <span data-ttu-id="d51d7-111">**存取特定的內部資料**。</span><span class="sxs-lookup"><span data-stu-id="d51d7-111">**Access to certain internal data**.</span></span> <span data-ttu-id="d51d7-112">由於複合檔案執行提供了撰寫特定資料類型的標準方式（例如摘要資訊），因此應用程式可以使用 COM 介面和 Api 來讀取此資料。</span><span class="sxs-lookup"><span data-stu-id="d51d7-112">Because the Compound Files implementation provides standard ways of writing certain types of data—summary information, for example—applications can read this data using COM interfaces and APIs.</span></span>

 

 




