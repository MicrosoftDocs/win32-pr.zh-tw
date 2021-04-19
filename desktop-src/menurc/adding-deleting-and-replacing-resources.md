---
title: 新增、刪除和取代資源
description: 本主題討論如何新增、刪除或取代資源。
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c12a1531e422efe44cbd0b3deca9f89838698
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968650"
---
# <a name="adding-deleting-and-replacing-resources"></a><span data-ttu-id="d9599-103">新增、刪除和取代資源</span><span class="sxs-lookup"><span data-stu-id="d9599-103">Adding, Deleting, and Replacing Resources</span></span>

<span data-ttu-id="d9599-104">應用程式必須經常新增、刪除或取代可執行檔中的資源。</span><span class="sxs-lookup"><span data-stu-id="d9599-104">Applications must frequently add, delete, or replace resources in executable files.</span></span> <span data-ttu-id="d9599-105">您可以使用兩種方法來完成這些工作。</span><span class="sxs-lookup"><span data-stu-id="d9599-105">Two methods can be used to accomplish these tasks.</span></span> <span data-ttu-id="d9599-106">第一個是編輯資源定義檔、重新編譯資源，然後將重新編譯的資源新增到應用程式的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d9599-106">The first is to edit the resource-definition file, recompile the resources, and add the recompiled resources to the application's executable file.</span></span> <span data-ttu-id="d9599-107">第二種方法是將資源資料直接複製到應用程式的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d9599-107">The second method is to copy the resource data directly into the application's executable file.</span></span>

<span data-ttu-id="d9599-108">例如，若要將英文版的應用程式當地語系化以用於挪威，可能需要使用挪威文來取代英文對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d9599-108">For example, to localize an English-language application for use in Norway, it may be necessary to replace the English dialog box with one using Norwegian.</span></span> <span data-ttu-id="d9599-109">開發人員會使用對話方塊編輯器或在資源定義檔中撰寫範本，建立適當的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d9599-109">A developer creates an appropriate dialog box by using a dialog box editor or by writing a template in the resource-definition file.</span></span> <span data-ttu-id="d9599-110">然後，開發人員會重新編譯資源，並將新的資源加入至應用程式的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d9599-110">The developer then recompiles the resources and adds the new resources to the application's executable file.</span></span>

<span data-ttu-id="d9599-111">但是，如果二進位格式有適當的對話方塊，開發人員可以使用下列函式，將資料直接複製到當地語系化的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d9599-111">If an appropriate dialog box exists in binary form, however, the developer can copy the data directly to the executable file being localized by using the following functions.</span></span> <span data-ttu-id="d9599-112">[**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)函式會建立要變更其資源之可執行檔的更新控制碼。</span><span class="sxs-lookup"><span data-stu-id="d9599-112">The [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) function creates an update handle to the executable file whose resources are to be changed.</span></span> <span data-ttu-id="d9599-113">[**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)函式會使用此控制碼來新增、刪除或取代可執行檔中的資源。</span><span class="sxs-lookup"><span data-stu-id="d9599-113">The [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) function uses this handle to add, delete, or replace a resource in the executable file.</span></span> <span data-ttu-id="d9599-114">[**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)函式會關閉控制碼。</span><span class="sxs-lookup"><span data-stu-id="d9599-114">The [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) function closes the handle.</span></span>

<span data-ttu-id="d9599-115">在 [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)建立可執行檔的更新控制碼之後，應用程式可以重複使用 [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) 來變更資源資料。</span><span class="sxs-lookup"><span data-stu-id="d9599-115">After an update handle to an executable file is created by [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea), an application can use [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) repeatedly to make changes to the resource data.</span></span> <span data-ttu-id="d9599-116">對 **UpdateResource** 的每個呼叫都會參與新增、刪除和取代的內部清單，但實際上不會將資料寫入至可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d9599-116">Each call to **UpdateResource** contributes to an internal list of additions, deletions, and replacements but does not actually write the data to the executable file.</span></span> <span data-ttu-id="d9599-117">[**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)會在關閉更新控制碼之前立即將累積的變更寫入至可執行檔。</span><span class="sxs-lookup"><span data-stu-id="d9599-117">Immediately before closing the update handle, [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) writes the accumulated changes to the executable file.</span></span>

<span data-ttu-id="d9599-118">有時候，應用程式必須從另一個檔案複製資源。</span><span class="sxs-lookup"><span data-stu-id="d9599-118">Sometimes, an application must copy resources from another file.</span></span> <span data-ttu-id="d9599-119">[更新資源](using-resources.md) 會顯示從檔案取得資源資料和其大小的範例。</span><span class="sxs-lookup"><span data-stu-id="d9599-119">[Updating Resources](using-resources.md) shows an example of obtaining the resource data and its size from a file.</span></span>

 

 




