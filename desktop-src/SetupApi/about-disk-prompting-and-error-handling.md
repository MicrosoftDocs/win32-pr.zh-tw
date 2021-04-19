---
description: 安裝函數可以產生對話方塊來處理常見的安裝狀況，並收集使用者的資訊。
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: 關於磁片提示和錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6c171d1e479d5d16198ba6d632848ff152f4ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972835"
---
# <a name="about-disk-prompting-and-error-handling"></a><span data-ttu-id="49d95-103">關於磁片提示和錯誤處理</span><span class="sxs-lookup"><span data-stu-id="49d95-103">About Disk Prompting and Error Handling</span></span>

<span data-ttu-id="49d95-104">雖然安裝函式不提供使用者介面，但有四個設定函數會產生對話方塊來處理常見的安裝狀況，並收集使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="49d95-104">Though the setup functions do not provide a user interface, there are four setup functions that generate dialog boxes to handle common installation situations and gather information from the user.</span></span> <span data-ttu-id="49d95-105">這些是： [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)、 [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)、 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)和 [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)。</span><span class="sxs-lookup"><span data-stu-id="49d95-105">These are: [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora), and [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).</span></span>

<span data-ttu-id="49d95-106">回呼常式可以呼叫這些函式來建立對話方塊，以協助處理其他安裝程式函數（例如 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 和 [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)）所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="49d95-106">Callback routines can call these functions to create dialog boxes to aid in processing notifications sent by other setup functions such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) and [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea).</span></span>

<span data-ttu-id="49d95-107">[**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)函式會提示使用者插入卸除式媒體、指定新的來源路徑，或取消安裝。</span><span class="sxs-lookup"><span data-stu-id="49d95-107">The [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function prompts the user to insert removable media, specify a new source path, or cancel the installation.</span></span> <span data-ttu-id="49d95-108">根據呼叫函式時所指定的旗標，應用程式可以為使用者提供其他選項。</span><span class="sxs-lookup"><span data-stu-id="49d95-108">The application can offer additional options to the user, depending on the flags specified when the function is called.</span></span> <span data-ttu-id="49d95-109">這些包括略過目前的檔案，或流覽新的來源路徑。</span><span class="sxs-lookup"><span data-stu-id="49d95-109">These include skipping the current file, or browsing for a new source path.</span></span>

<span data-ttu-id="49d95-110">這三個函式（ [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)、 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)和 [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)）會建立與使用者互動的對話方塊，以收集使用者的資訊，以瞭解如何在發生錯誤時繼續進行。</span><span class="sxs-lookup"><span data-stu-id="49d95-110">The three functions, [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora), and [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), create dialog boxes that interact with the user to gather information from the user on how to proceed when an error has occurred.</span></span>

<span data-ttu-id="49d95-111">[**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)函式會產生對話方塊，該對話方塊會詢問使用者如何從複製錯誤中復原。</span><span class="sxs-lookup"><span data-stu-id="49d95-111">The [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) function generates a dialog box that asks the user how to recover from a copy error.</span></span> <span data-ttu-id="49d95-112">使用者可以為複製作業指定新的來源路徑，或取消安裝。</span><span class="sxs-lookup"><span data-stu-id="49d95-112">The user can specify a new source path for the copy operation or cancel the installation.</span></span> <span data-ttu-id="49d95-113">視呼叫 **SetupCopyError** 期間指定的旗標而定，使用者也可以流覽新的來源路徑、查看錯誤詳細資料，或略過目前的檔案。</span><span class="sxs-lookup"><span data-stu-id="49d95-113">Depending on the flags specified during the call to **SetupCopyError**, the user may also be able to browse for a new source path, view error details, or skip the current file.</span></span>

<span data-ttu-id="49d95-114">此對話方塊會詢問使用者如何處理在檔案重新命名作業期間發生的錯誤，可以藉由呼叫 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)來產生。</span><span class="sxs-lookup"><span data-stu-id="49d95-114">A dialog box that asks the user how to process errors that occur during a file renaming operation can be generated by calling [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span></span> <span data-ttu-id="49d95-115">在此對話方塊中，使用者有機會重試作業、略過目前的重新命名作業或中止。</span><span class="sxs-lookup"><span data-stu-id="49d95-115">With this dialog box, the user has the opportunity to retry the operation, skip the current rename operation, or abort.</span></span>

<span data-ttu-id="49d95-116">[**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)函式會產生一個對話方塊，該對話方塊可收集使用者希望如何處理檔案刪除作業期間發生的錯誤的輸入。</span><span class="sxs-lookup"><span data-stu-id="49d95-116">The [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) function generates a dialog box that can gather input on how the user wishes to handle an error that occurred during a file deletion operation.</span></span> <span data-ttu-id="49d95-117">使用者可以選擇重試作業、略過目前的刪除作業或中止。</span><span class="sxs-lookup"><span data-stu-id="49d95-117">The user is given the options to retry the operation, skip the current delete operation, or abort.</span></span>

<span data-ttu-id="49d95-118">預設佇列回呼常式 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)會使用先前所述的四個函式來產生其使用者介面的元件，以及處理錯誤並提示新的媒體。</span><span class="sxs-lookup"><span data-stu-id="49d95-118">The default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), uses the previously mentioned four functions to generate parts of its user interface and to handle errors and prompt for new media.</span></span>

 

 



