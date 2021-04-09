---
title: 檔案傳輸一致性
description: BITS 保證根據檔案大小和時間戳記，它所傳輸的檔案版本是一致的，而不是內容 (位無法防止攔截式攻擊) 。
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839360"
---
# <a name="file-transfer-consistency"></a><span data-ttu-id="faf81-103">檔案傳輸一致性</span><span class="sxs-lookup"><span data-stu-id="faf81-103">File Transfer Consistency</span></span>

<span data-ttu-id="faf81-104">BITS 保證根據檔案大小和時間戳記，它所傳輸的檔案版本是一致的，而不是內容 (位無法防止攔截式攻擊) 。</span><span class="sxs-lookup"><span data-stu-id="faf81-104">BITS guarantees that the version of the file it transfers is consistent based on the file size and time stamp, not content (BITS does not protect against man-in-the-middle attacks).</span></span> <span data-ttu-id="faf81-105">若要自行驗證內容，您可以使用 [**IBackgroundCopyFile3：： GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) 方法取得包含所下載內容的檔案名，並使用您自己的機制來驗證內容，然後呼叫 [**IBackgroundCopyFile3：： SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) 方法，以指出檔案的內容是否有效。</span><span class="sxs-lookup"><span data-stu-id="faf81-105">To verify the contents yourself, you can use the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method to get the name of the file that contains the downloaded content, verify the contents using your own mechanism, and then call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method to indicate to BITS if the contents of the file is valid.</span></span> <span data-ttu-id="faf81-106">如果您將驗證狀態設為 **FALSE** ，且內容來自源伺服器，則作業會進入錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="faf81-106">If you set the validation state to **FALSE** and the content is from the origin server, the job goes into the error state.</span></span> <span data-ttu-id="faf81-107">如果內容來自對等，BITS 會從源伺服器下載檔案。</span><span class="sxs-lookup"><span data-stu-id="faf81-107">If the content is from a peer, BITS downloads the file from the origin server.</span></span>

<span data-ttu-id="faf81-108">針對下載，如果檔案大小或時間戳記在 BITS 傳輸檔案時變更，BITS 只會重新開機該檔案的傳送。</span><span class="sxs-lookup"><span data-stu-id="faf81-108">For downloads, if the file size or time stamp changes while BITS is transferring the file, BITS restarts the transfer of that file only.</span></span> <span data-ttu-id="faf81-109">例如，如果下載作業包含兩個檔案，而且 BITS 正在傳送第二個檔案時，伺服器上的檔案會更新，BITS 只會重新開機第二個檔案的傳送。</span><span class="sxs-lookup"><span data-stu-id="faf81-109">For example, if the download job contains two files and the files are updated on the server while BITS is transferring the second file, BITS restarts the transfer of the second file only.</span></span> <span data-ttu-id="faf81-110">第一個已成功傳輸的檔案不會更新，以反映新的變更。</span><span class="sxs-lookup"><span data-stu-id="faf81-110">The first file, which already transferred successfully, is not updated to reflect the new changes.</span></span>

<span data-ttu-id="faf81-111">請注意，如果您擁有從伺服器下載的檔案，則應該為檔案的每個新版本建立新的 URL。</span><span class="sxs-lookup"><span data-stu-id="faf81-111">Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file.</span></span> <span data-ttu-id="faf81-112">如果您針對新版本的檔案使用相同的 URL，部分 proxy 伺服器可能會從其快取中提供過時的資料，因為如果檔案已過時，就不會向源伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="faf81-112">If you use the same URL for new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale.</span></span>

<span data-ttu-id="faf81-113">針對上傳，如果檔案大小或時間戳記在檔案傳輸期間有所變更，BITS 會產生錯誤，而且作業會處於「BG \_ 工作 \_ 狀態」 \_ 錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="faf81-113">For uploads, if the file size or time stamp changes during the file transfer, BITS generates an error and the job is placed in the BG\_JOB\_STATE\_ERROR state.</span></span>

<span data-ttu-id="faf81-114">當一或多個使用者要求相同的檔案傳送到相同的位置時，BITS 不會同步處理傳輸要求。</span><span class="sxs-lookup"><span data-stu-id="faf81-114">BITS does not synchronize transfer requests when one or more users request that the same file be transferred to the same location.</span></span> <span data-ttu-id="faf81-115">BITS 會分別傳送每個要求的檔案。</span><span class="sxs-lookup"><span data-stu-id="faf81-115">BITS transfers the file for each request separately.</span></span>

 

 




