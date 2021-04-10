---
title: FTP 會話
description: WinINet 可讓應用程式在 ftp 伺服器上流覽和操作目錄和檔案。 因為 CERN proxy 不支援 FTP，所以使用 CERN proxy 的應用程式必須使用 InternetOpenUrl 函數。
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023771"
---
# <a name="ftp-sessions"></a><span data-ttu-id="03ac8-104">FTP 會話</span><span class="sxs-lookup"><span data-stu-id="03ac8-104">FTP Sessions</span></span>

<span data-ttu-id="03ac8-105">WinINet 可讓應用程式在 ftp 伺服器上流覽和操作目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-105">WinINet enables applications to navigate and manipulate directories and files on an ftp server.</span></span> <span data-ttu-id="03ac8-106">因為 CERN proxy 不支援 FTP，所以使用 CERN proxy 的應用程式必須使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數。</span><span class="sxs-lookup"><span data-stu-id="03ac8-106">Because CERN proxies do not support FTP, applications that use a CERN proxy exclusively must use the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> <span data-ttu-id="03ac8-107">如需如何使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)的詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-107">For more information about how to use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="03ac8-108">若要開始 FTP 會話，請使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 來建立會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-108">To begin an FTP session, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to create the session handle.</span></span>

<span data-ttu-id="03ac8-109">WinINet 可讓您在 FTP 伺服器上執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="03ac8-109">WinINet enables you to perform the following actions on an FTP server:</span></span>

-   <span data-ttu-id="03ac8-110">在目錄之間流覽。</span><span class="sxs-lookup"><span data-stu-id="03ac8-110">Navigate between directories.</span></span>
-   <span data-ttu-id="03ac8-111">列舉、建立、移除和重新命名目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-111">Enumerate, create, remove, and rename directories.</span></span>
-   <span data-ttu-id="03ac8-112">重新命名、上傳、下載及刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-112">Rename, upload, download, and delete files.</span></span>

<span data-ttu-id="03ac8-113">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)和 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)函式會提供導覽。</span><span class="sxs-lookup"><span data-stu-id="03ac8-113">Navigation is provided by the [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions.</span></span> <span data-ttu-id="03ac8-114">這些函式會利用前一次呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所建立的會話控制碼，判斷應用程式目前所在的目錄，或變更至不同的子目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-114">These functions utilize the session handle created by a previous call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to determine which directory the application is currently in, or to change to a different subdirectory.</span></span>

<span data-ttu-id="03ac8-115">目錄列舉是使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 和 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 函數來執行。</span><span class="sxs-lookup"><span data-stu-id="03ac8-115">Directory enumeration is performed by using the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="03ac8-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 會使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所建立的會話控制碼來尋找符合指定搜尋準則的第一個檔案，並傳回可繼續目錄列舉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to find the first file that matches the given search criteria and returns a handle to continue the directory enumeration.</span></span> <span data-ttu-id="03ac8-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 會使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 傳回的控制碼來傳回符合原始搜尋準則的下一個檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) uses the handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) to return the next file that matches the original search criteria.</span></span> <span data-ttu-id="03ac8-118">除非目錄中沒有其他檔案，否則應用程式應繼續呼叫 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-118">The application should continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until there are no more files left in the directory.</span></span>

<span data-ttu-id="03ac8-119">使用 [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) 函式來建立新的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-119">Use the [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function to create new directories.</span></span> <span data-ttu-id="03ac8-120">此函式會使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所建立的會話控制碼，並建立傳遞給函式之字串所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-120">This function uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and creates the directory specified by the string passed to the function.</span></span> <span data-ttu-id="03ac8-121">字串可以包含相對於目前的目錄的目錄名稱，或是完整的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="03ac8-121">The string can contain a directory name relative to the current directory, or a fully qualified directory path.</span></span>

<span data-ttu-id="03ac8-122">若要重新命名檔案或目錄，應用程式可以呼叫 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-122">To rename either files or directories, the application can call [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span></span> <span data-ttu-id="03ac8-123">此函式會將原始名稱取代為傳遞給函式的新名稱。</span><span class="sxs-lookup"><span data-stu-id="03ac8-123">This function replaces the original name with the new name passed to the function.</span></span> <span data-ttu-id="03ac8-124">檔案或目錄的名稱可以相對於目前的目錄或完整名稱。</span><span class="sxs-lookup"><span data-stu-id="03ac8-124">The name of the file or directory can be relative to the current directory, or a fully qualified name.</span></span>

<span data-ttu-id="03ac8-125">若要在 FTP 伺服器上上傳或放置檔案，應用程式可以使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) 或 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (以及 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-125">To upload or place files on an FTP server, the application can use either [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (along with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span></span> <span data-ttu-id="03ac8-126">如果檔案已存在於本機，則可以使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) ，而如果需要將資料寫入 FTP 伺服器上的檔案，則可以使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)和 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) can be used if the file already exists locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) can be used if data needs to be written to a file on the FTP server.</span></span>

<span data-ttu-id="03ac8-127">若要下載或取得檔案，應用程式可以使用 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 或 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (搭配 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-127">To download or get files, the application can use either [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span></span> <span data-ttu-id="03ac8-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 是用來從 FTP 伺服器取出檔案並將它儲存在本機，而 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 可以用來控制下載資訊的 (例如，應用程式可以在編輯方塊中顯示資訊) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) is used to retrieve a file from an FTP server and store it locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can be used to control where the downloaded information is going (for example, the application could display the information in an edit box).</span></span>

<span data-ttu-id="03ac8-129">使用 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) 函數刪除 FTP 伺服器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-129">Delete files on an FTP server by using the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="03ac8-130">此函式會從 FTP 伺服器移除相對於目前的目錄或完整檔案名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="03ac8-130">This function removes a file name that is relative either to the current directory or to a fully qualified file name from the FTP server.</span></span> <span data-ttu-id="03ac8-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) 需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)傳回的會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requires a session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>

## <a name="ftp-function-handles"></a><span data-ttu-id="03ac8-132">FTP 函數控制碼</span><span class="sxs-lookup"><span data-stu-id="03ac8-132">FTP Function Handles</span></span>

<span data-ttu-id="03ac8-133">若要正常運作，FTP 函數需要特定類型的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-133">To work properly, the FTP functions require certain types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="03ac8-134">這些控制碼必須以特定順序建立，從 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所建立的根控制碼開始。</span><span class="sxs-lookup"><span data-stu-id="03ac8-134">These handles must be created in a specific order, starting with the root handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="03ac8-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 接著可以建立 FTP 會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) can then create an FTP session handle.</span></span>

<span data-ttu-id="03ac8-136">下圖顯示相依于 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所傳回之 FTP 會話控制碼的函式。</span><span class="sxs-lookup"><span data-stu-id="03ac8-136">The following diagram shows the functions that are dependent on the FTP session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="03ac8-137">陰影方塊代表會傳回 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 HINTERNET 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-137">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the HINTERNET handle created by the function on which they depend.</span></span>

![ftp 函數相依于 internetconnect 所傳回的 ftp 會話控制碼](images/ax-wnt06.png)

<span data-ttu-id="03ac8-139">下圖顯示兩個函式，這些函式會傳回 [HINTERNET](appendix-a-hinternet-handles.md) 控制碼和相依的函式。</span><span class="sxs-lookup"><span data-stu-id="03ac8-139">The following diagram shows the two functions that return [HINTERNET](appendix-a-hinternet-handles.md) handles and the functions that are dependent on them.</span></span> <span data-ttu-id="03ac8-140">陰影方塊代表會傳回 **HINTERNET** 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-140">The shaded boxes represent functions that return **HINTERNET** handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![傳回 hinternet 控制碼的 ftp 函數](images/ax-wnt03.png)

<span data-ttu-id="03ac8-142">如需詳細資訊，請參閱 [HINTERNET 控制碼](appendix-a-hinternet-handles.md)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-142">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-for-ftp-sessions"></a><span data-ttu-id="03ac8-143">使用適用于 FTP 會話的 WinINet 函數</span><span class="sxs-lookup"><span data-stu-id="03ac8-143">Using the WinINet Functions for FTP Sessions</span></span>

<span data-ttu-id="03ac8-144">FTP 會話期間使用下列函數。</span><span class="sxs-lookup"><span data-stu-id="03ac8-144">The following functions are used during FTP sessions.</span></span> <span data-ttu-id="03ac8-145">CERN proxy 無法辨識這些函數。</span><span class="sxs-lookup"><span data-stu-id="03ac8-145">These functions are not recognized by CERN proxies.</span></span> <span data-ttu-id="03ac8-146">必須透過 CERN proxy 運作的應用程式應該使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 並直接存取資源。</span><span class="sxs-lookup"><span data-stu-id="03ac8-146">Applications that must function through CERN proxies should use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and access the resources directly.</span></span> <span data-ttu-id="03ac8-147">如需直接存取資源的詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-147">For more information on direct resource access, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>



| <span data-ttu-id="03ac8-148">函式</span><span class="sxs-lookup"><span data-stu-id="03ac8-148">Function</span></span>                                                 | <span data-ttu-id="03ac8-149">描述</span><span class="sxs-lookup"><span data-stu-id="03ac8-149">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03ac8-150">**FtpCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="03ac8-150">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | <span data-ttu-id="03ac8-151">在伺服器上建立新的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-151">Creates a new directory on the server.</span></span> <span data-ttu-id="03ac8-152">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-152">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                  |
| [<span data-ttu-id="03ac8-153">**FtpDeleteFile**</span><span class="sxs-lookup"><span data-stu-id="03ac8-153">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | <span data-ttu-id="03ac8-154">從伺服器刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-154">Deletes a file from the server.</span></span> <span data-ttu-id="03ac8-155">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-155">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                         |
| [<span data-ttu-id="03ac8-156">**FtpFindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="03ac8-156">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | <span data-ttu-id="03ac8-157">在目前的目錄中開始檔案列舉或檔案搜尋。</span><span class="sxs-lookup"><span data-stu-id="03ac8-157">Starts file enumeration or file search in the current directory.</span></span> <span data-ttu-id="03ac8-158">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-158">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>        |
| [<span data-ttu-id="03ac8-159">**FtpGetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="03ac8-159">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | <span data-ttu-id="03ac8-160">傳回伺服器上用戶端的目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-160">Returns the client's current directory on the server.</span></span> <span data-ttu-id="03ac8-161">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-161">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="03ac8-162">**FtpGetFile**</span><span class="sxs-lookup"><span data-stu-id="03ac8-162">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | <span data-ttu-id="03ac8-163">從伺服器抓取檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-163">Retrieves a file from the server.</span></span> <span data-ttu-id="03ac8-164">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-164">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                       |
| [<span data-ttu-id="03ac8-165">**FtpOpenFile**</span><span class="sxs-lookup"><span data-stu-id="03ac8-165">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | <span data-ttu-id="03ac8-166">起始存取伺服器上的檔案以進行讀取或寫入。</span><span class="sxs-lookup"><span data-stu-id="03ac8-166">Initiates access to a file on the server for either reading or writing.</span></span> <span data-ttu-id="03ac8-167">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-167">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> |
| [<span data-ttu-id="03ac8-168">**FtpPutFile**</span><span class="sxs-lookup"><span data-stu-id="03ac8-168">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | <span data-ttu-id="03ac8-169">將檔案寫入伺服器。</span><span class="sxs-lookup"><span data-stu-id="03ac8-169">Writes a file to the server.</span></span> <span data-ttu-id="03ac8-170">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-170">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                            |
| [<span data-ttu-id="03ac8-171">**FtpRemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="03ac8-171">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | <span data-ttu-id="03ac8-172">刪除伺服器上的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-172">Deletes a directory on the server.</span></span> <span data-ttu-id="03ac8-173">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-173">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                      |
| [<span data-ttu-id="03ac8-174">**FtpRenameFile**</span><span class="sxs-lookup"><span data-stu-id="03ac8-174">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | <span data-ttu-id="03ac8-175">重新命名伺服器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-175">Renames a file on the server.</span></span> <span data-ttu-id="03ac8-176">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-176">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                           |
| [<span data-ttu-id="03ac8-177">**FtpSetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="03ac8-177">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | <span data-ttu-id="03ac8-178">變更用戶端在伺服器上的目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-178">Changes the client's current directory on the server.</span></span> <span data-ttu-id="03ac8-179">此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-179">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="03ac8-180">**InternetWriteFile**</span><span class="sxs-lookup"><span data-stu-id="03ac8-180">**InternetWriteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | <span data-ttu-id="03ac8-181">將資料寫入伺服器上已開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-181">Writes data to an open file on the server.</span></span> <span data-ttu-id="03ac8-182">此函數需要 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-182">This function requires a handle created by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span></span>                                      |



 

### <a name="starting-an-ftp-session"></a><span data-ttu-id="03ac8-183">啟動 FTP 會話</span><span class="sxs-lookup"><span data-stu-id="03ac8-183">Starting an FTP Session</span></span>

<span data-ttu-id="03ac8-184">應用程式會在 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)建立的控制碼上呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ，以建立 FTP 會話。</span><span class="sxs-lookup"><span data-stu-id="03ac8-184">The application establishes an FTP session by calling [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) on a handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="03ac8-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 需要 [伺服器名稱]、[埠號碼]、[使用者名稱]、[密碼] 和 [服務類型] (必須設定為 [網際網路 \_ 服務 \_ FTP]) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) needs the server name, port number, user name, password, and service type (which must be set to INTERNET\_SERVICE\_FTP).</span></span> <span data-ttu-id="03ac8-186">針對被動 FTP 語義，應用程式也必須設定 [網際網路 \_ 旗標 \_ 被動](api-flags.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="03ac8-186">For passive FTP semantics, the application must also set the [INTERNET\_FLAG\_PASSIVE](api-flags.md) flag.</span></span>

<span data-ttu-id="03ac8-187">網際網路 \_ 預設 \_ FTP \_ 埠和網際網路通訊 \_ \_ 埠 \_ 編號值可以用於埠號碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-187">The INTERNET\_DEFAULT\_FTP\_PORT and INTERNET\_INVALID\_PORT\_NUMBER values can be used for the port number.</span></span> <span data-ttu-id="03ac8-188">網際網路 \_ 預設 \_ ftp \_ 埠使用預設的 ftp 埠，但仍然必須設定服務類型。</span><span class="sxs-lookup"><span data-stu-id="03ac8-188">INTERNET\_DEFAULT\_FTP\_PORT uses the default FTP port, but the service type still must be set.</span></span> <span data-ttu-id="03ac8-189">網際網路 \_ 無效 \_ \_ 的埠號碼會使用指定之服務類型的預設值。</span><span class="sxs-lookup"><span data-stu-id="03ac8-189">INTERNET\_INVALID\_PORT\_NUMBER uses the default value for the indicated service type.</span></span>

<span data-ttu-id="03ac8-190">您可以將使用者名稱和密碼的值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03ac8-190">The values for the user name and password can be set to **NULL**.</span></span> <span data-ttu-id="03ac8-191">如果這兩個值都設定為 **Null**， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會使用「匿名」作為使用者名稱，並使用使用者的電子郵件地址做為密碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-191">If both values are set to **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses "anonymous" for the user name, and the user's email address for the password.</span></span> <span data-ttu-id="03ac8-192">如果只有密碼設定為 **Null**，則會使用傳遞至 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 的使用者名稱做為使用者名稱，並使用空字串作為密碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-192">If only the password is set to **NULL**, the user name passed to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) is used for the user name, and an empty string is used for the password.</span></span> <span data-ttu-id="03ac8-193">如果兩個值都不是 **Null**，就會使用提供給 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-193">If neither value is **NULL**, the user name and password given to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) are used.</span></span>

### <a name="enumerating-directories"></a><span data-ttu-id="03ac8-194">列舉目錄</span><span class="sxs-lookup"><span data-stu-id="03ac8-194">Enumerating Directories</span></span>

<span data-ttu-id="03ac8-195">您必須透過 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)建立控制碼，以列舉 FTP 伺服器上的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-195">Enumeration of a directory on an FTP server requires the creation of a handle by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="03ac8-196">這個控制碼是 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立之會話控制碼的分支。</span><span class="sxs-lookup"><span data-stu-id="03ac8-196">This handle is a branch of the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="03ac8-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 會找出伺服器上的第一個檔案或目錄，並將它傳回 [**WIN32 \_ FIND \_ 資料**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) 結構中。</span><span class="sxs-lookup"><span data-stu-id="03ac8-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) locates the first file or directory on the server and returns it in a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="03ac8-198">使用 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 直到傳回 [**錯誤的 \_ 檔案 \_ \_**](wininet-errors.md)為止。</span><span class="sxs-lookup"><span data-stu-id="03ac8-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until it returns [**ERROR\_NO\_MORE\_FILES**](wininet-errors.md).</span></span> <span data-ttu-id="03ac8-199">這個方法會尋找伺服器上的所有後續檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-199">This method finds all subsequent files and directories on the server.</span></span> <span data-ttu-id="03ac8-200">如需 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)的詳細資訊，請參閱 [尋找下一個](common-functions.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-200">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="03ac8-201">若要判斷 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)或 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)取出的檔案是否為目錄，請檢查 [**WIN32 \_ FIND \_ 資料**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa)結構的 **dwFileAttributes** 成員，看看它是否等於檔 \_ 屬性 \_ 目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-201">To determine if the file retrieved by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) or [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) is a directory, check the **dwFileAttributes** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure to see if it is equal to FILE\_ATTRIBUTE\_DIRECTORY.</span></span>

<span data-ttu-id="03ac8-202">如果應用程式在 FTP 伺服器上進行變更，或 FTP 伺服器經常變更，則不應在 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)中設定「[網際網路 \_ 旗 \_ \_ \_](api-flags.md)標」和「[網際網路 \_ 旗標 \_ 重載](api-flags.md)」旗標。</span><span class="sxs-lookup"><span data-stu-id="03ac8-202">If the application makes changes on the FTP server or if the FTP server changes frequently, the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) and [INTERNET\_FLAG\_RELOAD](api-flags.md) flags should be set in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="03ac8-203">這些旗標可確保從 FTP 伺服器取出的目錄資訊是最新的。</span><span class="sxs-lookup"><span data-stu-id="03ac8-203">These flags ensure that the directory information being retrieved from the FTP server is current.</span></span>

<span data-ttu-id="03ac8-204">在應用程式完成目錄列舉之後，應用程式必須在 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)建立的控制碼上呼叫 [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-204">After the application completes the directory enumeration, the application must make a call to [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle created by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="03ac8-205">在該控制碼關閉之前，應用程式無法在 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)建立的會話控制碼上再次呼叫 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-205">Until that handle is closed, the application cannot call [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) again on the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="03ac8-206">如果在前一次呼叫相同的函式之前，對相同的會話控制碼進行 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 呼叫，此函式會失敗， [並 \_ 傳回錯誤 FTP \_ 傳輸 \_ \_ 進行中](wininet-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-206">If a call to [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) is made on the same session handle before the previous call to the same function is closed, the function fails, returning [ERROR\_FTP\_TRANSFER\_IN\_PROGRESS](wininet-errors.md).</span></span>

<span data-ttu-id="03ac8-207">下列範例會將 FTP 目錄的內容列舉為清單方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="03ac8-207">The following example enumerates the contents of an FTP directory into a list box control.</span></span> <span data-ttu-id="03ac8-208">*HConnection* 參數是 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式在建立 FTP 會話之後所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-208">The *hConnection* parameter is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span> <span data-ttu-id="03ac8-209">此範例中所參考 InternetErrorOut 函式的範例原始程式碼可在 [處理錯誤](appendix-c-handling-errors.md)主題中找到。</span><span class="sxs-lookup"><span data-stu-id="03ac8-209">Sample source code for the InternetErrorOut function referenced in this example can be found in the [Handling Errors](appendix-c-handling-errors.md)topic.</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a><span data-ttu-id="03ac8-210">流覽目錄</span><span class="sxs-lookup"><span data-stu-id="03ac8-210">Navigating Directories</span></span>

<span data-ttu-id="03ac8-211">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)和 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)函式會處理目錄導覽。</span><span class="sxs-lookup"><span data-stu-id="03ac8-211">The [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions handle directory navigation.</span></span>

<span data-ttu-id="03ac8-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) 會傳回 FTP 伺服器上應用程式的目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) returns the application's current directory on the FTP server.</span></span> <span data-ttu-id="03ac8-213">包含 FTP 伺服器根目錄的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="03ac8-213">The directory path from the root directory on the FTP server is included.</span></span>

<span data-ttu-id="03ac8-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) 會變更伺服器上的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the working directory on the server.</span></span> <span data-ttu-id="03ac8-215">傳遞至 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) 的目錄資訊可以是相對於目前的目錄的部分或完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="03ac8-215">The directory information passed to [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) can be either a partially or fully qualified path name relative to the current directory.</span></span> <span data-ttu-id="03ac8-216">例如，如果應用程式目前位於目錄 "public/info"，且路徑為 "ftp/example"， [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) 會將目前的目錄變更為 "public/info/ftp/example"。</span><span class="sxs-lookup"><span data-stu-id="03ac8-216">For example, if the application is currently in the directory "public/info" and the path is "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the current directory to "public/info/ftp/example".</span></span>

<span data-ttu-id="03ac8-217">下列範例會使用由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所傳回的 FTP 會話控制碼 hConnection。</span><span class="sxs-lookup"><span data-stu-id="03ac8-217">The following example uses the FTP session handle hConnection, which is returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="03ac8-218">新的目錄名稱是取自父對話方塊的 [編輯] 方塊，其 IDC 會在 *nDirNameId* 參數中傳遞。</span><span class="sxs-lookup"><span data-stu-id="03ac8-218">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="03ac8-219">在進行目錄變更之前，此函式會抓取目前的目錄，並將它儲存在相同的編輯方塊中。</span><span class="sxs-lookup"><span data-stu-id="03ac8-219">Before the directory change is made, the function retrieves the current directory and stores it in the same edit box.</span></span> <span data-ttu-id="03ac8-220">上述 DisplayFtpDir 函式的來源程式代碼會在上方列出。</span><span class="sxs-lookup"><span data-stu-id="03ac8-220">The souce code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a><span data-ttu-id="03ac8-221">操作 FTP 伺服器上的目錄</span><span class="sxs-lookup"><span data-stu-id="03ac8-221">Manipulating Directories on an FTP Server</span></span>

<span data-ttu-id="03ac8-222">WinINet 提供在 FTP 伺服器上建立和移除目錄的功能，應用程式具有必要的許可權。</span><span class="sxs-lookup"><span data-stu-id="03ac8-222">WinINet provides the capability to create and remove directories on an FTP server to which the application has the necessary privileges.</span></span> <span data-ttu-id="03ac8-223">如果應用程式必須以特定的使用者名稱和密碼登入伺服器，則在建立 FTP 會話控制碼時，可以在 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 中使用這些值。</span><span class="sxs-lookup"><span data-stu-id="03ac8-223">If the application must log on to a server with a specific user name and password, the values can be used in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) when creating the FTP session handle.</span></span>

<span data-ttu-id="03ac8-224">[**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)函式會採用有效的 FTP 會話控制碼和以 **null** 終止的字串，其中包含相對於目前的目錄的完整路徑或名稱，並在 FTP 伺服器上建立目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-224">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function takes a valid FTP session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and creates a directory on the FTP server.</span></span>

<span data-ttu-id="03ac8-225">下列範例顯示兩個不同的 [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)呼叫。</span><span class="sxs-lookup"><span data-stu-id="03ac8-225">The following example shows two separate calls to [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span></span> <span data-ttu-id="03ac8-226">在這兩個範例中，hFtpSession 是由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函數所建立的會話控制碼，而根目錄是目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-226">In both examples, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span>

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

<span data-ttu-id="03ac8-227">[**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)函式會採用會話控制碼和以 **null** 終止的字串，其中包含相對於目前的目錄的完整路徑或名稱，然後從 FTP 伺服器移除該目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-227">The [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) function takes a session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and removes that directory from the FTP server.</span></span>

<span data-ttu-id="03ac8-228">下列範例顯示兩個對 [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)的呼叫範例。</span><span class="sxs-lookup"><span data-stu-id="03ac8-228">The following example shows two sample calls to [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span></span> <span data-ttu-id="03ac8-229">在這兩個呼叫中，hFtpSession 是由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函數所建立的會話控制碼，而根目錄是目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-229">In both calls, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span> <span data-ttu-id="03ac8-230">根目錄中有一個名為 "test" 的目錄，以及 "test" 目錄中名為 "example" 的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-230">There is a directory called "test" in the root directory and a directory called "example" in the "test" directory.</span></span>

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



<span data-ttu-id="03ac8-231">下列範例會在 FTP 伺服器上建立新的目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-231">The following example creates a new directory on the FTP server.</span></span> <span data-ttu-id="03ac8-232">新的目錄名稱是取自父對話方塊的 [編輯] 方塊，其 IDC 會在 *nDirNameId* 參數中傳遞。</span><span class="sxs-lookup"><span data-stu-id="03ac8-232">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="03ac8-233">建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-233">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="03ac8-234">在結尾處呼叫 DisplayFtpDir 函式的原始程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="03ac8-234">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



<span data-ttu-id="03ac8-235">下列範例會從 FTP 伺服器刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-235">The following example deletes a directory from the FTP server.</span></span> <span data-ttu-id="03ac8-236">要刪除的目錄名稱是取自父對話方塊中的 [編輯] 方塊，其 IDC 會傳入 *nDirNameId* 參數。</span><span class="sxs-lookup"><span data-stu-id="03ac8-236">The name of the directory to be deleted is taken from the edit box in the parent dialog whose IDC is passed into the *nDirNameId* parameter.</span></span> <span data-ttu-id="03ac8-237">建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-237">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="03ac8-238">在結尾處呼叫 DisplayFtpDir 函式的原始程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="03ac8-238">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a><span data-ttu-id="03ac8-239">取得 FTP 伺服器上的檔案</span><span class="sxs-lookup"><span data-stu-id="03ac8-239">Getting Files on an FTP Server</span></span>

<span data-ttu-id="03ac8-240">有三種方法可從 FTP 伺服器上取出檔案：</span><span class="sxs-lookup"><span data-stu-id="03ac8-240">There are three methods for retrieving files from an FTP server:</span></span>

-   <span data-ttu-id="03ac8-241">使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="03ac8-242">使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="03ac8-243">使用 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span></span>

<span data-ttu-id="03ac8-244">如需使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 函數的詳細資訊，請參閱 [讀取](common-functions.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-244">For more information about using the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function, see [Reading Files](common-functions.md).</span></span>

<span data-ttu-id="03ac8-245">如果檔案的 URL 可用，應用程式可以呼叫 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 來連接到該 url，然後使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 來控制檔案的下載。</span><span class="sxs-lookup"><span data-stu-id="03ac8-245">If the URL of the file is available, the application can call [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to connect to that URL, then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to control the download of the file.</span></span> <span data-ttu-id="03ac8-246">這可讓應用程式更嚴密地控制下載，而且非常適合在 FTP 伺服器上不需要進行其他作業的情況下。</span><span class="sxs-lookup"><span data-stu-id="03ac8-246">This allows the application tighter control over the download and is ideal for situations where no other operations need to be made on the FTP server.</span></span> <span data-ttu-id="03ac8-247">如需如何直接存取資源的詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-247">For more information about how to directly access resources, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="03ac8-248">如果應用程式已使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)建立與伺服器的 FTP 會話控制碼，則應用程式可以使用現有的檔案名和本機儲存之檔案的新名稱來呼叫 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 。</span><span class="sxs-lookup"><span data-stu-id="03ac8-248">If the application has established an FTP session handle to the server with [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), the application can call [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with the existing file name and with a new name for the locally stored file.</span></span> <span data-ttu-id="03ac8-249">然後，應用程式可以使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 來下載檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-249">The application can then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to download the file.</span></span> <span data-ttu-id="03ac8-250">如此一來，應用程式就能更嚴密地控制下載內容並保持與 FTP 伺服器的連接，因此可以執行更多命令。</span><span class="sxs-lookup"><span data-stu-id="03ac8-250">This allows the application tighter control over the download and keeps the connection to the FTP server, so more commands can be executed.</span></span>

<span data-ttu-id="03ac8-251">如果應用程式不需要嚴格控制下載，則應用程式可以使用 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 與 FTP 會話控制碼、遠端檔案名和本機檔案名來取出檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-251">If the application does not need tight control over the download, the application can use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) with the FTP session handle, remote file name, and local file name to retrieve the file.</span></span> <span data-ttu-id="03ac8-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 會執行所有與從 FTP 伺服器讀取檔案並儲存在本機的相關簿記和負擔。</span><span class="sxs-lookup"><span data-stu-id="03ac8-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) performs all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally.</span></span>

<span data-ttu-id="03ac8-253">下列範例會從 FTP 伺服器抓取檔案，並將它儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="03ac8-253">The following example retrieves a file from an FTP server and saves it locally.</span></span> <span data-ttu-id="03ac8-254">FTP 伺服器上的檔案名是取自父對話方塊中的 [編輯] 方塊，其 IDC 會在 *nFtpFileNameId* 參數中傳遞，而儲存檔案的本機名稱則是取自在 *nLocalFileNameId* 參數中傳遞其 idc 的編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="03ac8-254">The name of the file on the FTP server is taken from the edit box in the parent dialog whose IDC is passed in the *nFtpFileNameId* parameter, and the local name under which the file is saved is taken from the edit box whose IDC is passed in the *nLocalFileNameId* parameter.</span></span> <span data-ttu-id="03ac8-255">建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-255">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a><span data-ttu-id="03ac8-256">將檔案放在 FTP 伺服器上</span><span class="sxs-lookup"><span data-stu-id="03ac8-256">Placing Files on an FTP Server</span></span>

<span data-ttu-id="03ac8-257">有兩種方法可將檔案放在 FTP 伺服器上：</span><span class="sxs-lookup"><span data-stu-id="03ac8-257">There are two methods for placing a file on an FTP server:</span></span>

-   <span data-ttu-id="03ac8-258">搭配使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 與 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span></span>
-   <span data-ttu-id="03ac8-259">使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>

<span data-ttu-id="03ac8-260">必須將資料傳送至 FTP 伺服器的應用程式，但沒有包含所有資料的本機檔案，則應該使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 在 ftp 伺服器上建立並開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-260">An application that must send data to an FTP server, but does not have a local file that contains all the data, should use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) to create and open a file on the ftp server.</span></span> <span data-ttu-id="03ac8-261">然後，應用程式可以使用 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) 將資訊上傳至檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-261">The application then can use [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) to upload the information to the file.</span></span>

<span data-ttu-id="03ac8-262">如果檔案已存在於本機，則應用程式可以使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) 將檔案上傳到 FTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="03ac8-262">If the file already exists locally, the application can use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) to upload the file to the FTP server.</span></span> <span data-ttu-id="03ac8-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) 會執行將本機檔案上傳到遠端 FTP 伺服器所產生的所有負擔。</span><span class="sxs-lookup"><span data-stu-id="03ac8-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) performs all the overhead that goes with uploading a local file to a remote FTP server.</span></span>

<span data-ttu-id="03ac8-264">下列範例會將本機檔案複製到 FTP 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="03ac8-264">The following example copies a local file onto the FTP server.</span></span> <span data-ttu-id="03ac8-265">檔案的本機名稱是取自父對話方塊中的 [編輯] 方塊，其 IDC 是在 *nLocalFileNameId* 參數中傳遞，而檔案儲存在 FTP 伺服器上的名稱則是取自在 *nFtpFileNameId* 參數中傳遞其 idc 的編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="03ac8-265">The local name of the file is taken from the edit box in the parent dialog whose IDC is passed in the *nLocalFileNameId* parameter, and the name under which the file is saved on the FTP server is taken from the edit box whose IDC is passed in the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="03ac8-266">建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-266">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a><span data-ttu-id="03ac8-267">從 FTP 伺服器刪除檔案</span><span class="sxs-lookup"><span data-stu-id="03ac8-267">Deleting Files from an FTP Server</span></span>

<span data-ttu-id="03ac8-268">若要從 FTP 伺服器刪除檔案，請使用 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="03ac8-268">To delete a file from an FTP server, use the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="03ac8-269">呼叫應用程式必須具有從 FTP 伺服器刪除檔案的必要許可權。</span><span class="sxs-lookup"><span data-stu-id="03ac8-269">The calling application must have the necessary privileges to delete a file from the FTP server.</span></span>

<span data-ttu-id="03ac8-270">下列範例會從 FTP 伺服器刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="03ac8-270">The following example deletes a file from the FTP server.</span></span> <span data-ttu-id="03ac8-271">要刪除之檔案的名稱是取自父對話方塊中的 [編輯] 方塊，其 IDC 會以 int 傳遞 *nFtpFileNameId* 參數。</span><span class="sxs-lookup"><span data-stu-id="03ac8-271">The name of the file to be deleted is taken from the edit box in the parent dialog whose IDC is passed int the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="03ac8-272">建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-272">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="03ac8-273">由於此函式不會重新整理檔案清單或目錄顯示，因此呼叫進程應該在成功刪除時這樣做。</span><span class="sxs-lookup"><span data-stu-id="03ac8-273">Since this function does not refresh file listings or directory display, the calling process should do so upon successful deletion.</span></span>


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a><span data-ttu-id="03ac8-274">重新命名 FTP 伺服器上的檔案和目錄</span><span class="sxs-lookup"><span data-stu-id="03ac8-274">Renaming Files and Directories on an FTP Server</span></span>

<span data-ttu-id="03ac8-275">您可以使用 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) 函式來重新命名 FTP 伺服器上的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-275">Files and directories on an FTP server can be renamed using the [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) function.</span></span> <span data-ttu-id="03ac8-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) 接受兩個以 **null** 終止的字串，其中包含相對於目前的目錄的部分或完整名稱。</span><span class="sxs-lookup"><span data-stu-id="03ac8-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepts two **null**-terminated strings that contain either partially or fully qualified names relative to the current directory.</span></span> <span data-ttu-id="03ac8-277">函式會將第一個字串所指定的檔案名，變更為第二個字串所指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="03ac8-277">The function changes the name of the file designated by the first string to the name designated by the second string.</span></span>

<span data-ttu-id="03ac8-278">下列範例會重新命名 FTP 伺服器上的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="03ac8-278">The following example renames a file or directory on the FTP server.</span></span> <span data-ttu-id="03ac8-279">檔案或目錄的目前名稱取自父對話方塊中的 [編輯] 方塊，其 IDC 會在 *nOldFileNameId* 參數中傳遞，而新的名稱則是取自在 *nNewFileNameId* 參數中傳遞其 idc 的編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="03ac8-279">The current name of the file or directory is taken from the edit box in the parent dialog whose IDC is passed in the *nOldFileNameId* parameter, and the new name is taken from the edit box whose IDC is passed in the *nNewFileNameId* parameter.</span></span> <span data-ttu-id="03ac8-280">建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="03ac8-280">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="03ac8-281">由於此函式不會重新整理檔案清單或目錄顯示，因此呼叫進程應該在成功重新命名時這麼做。</span><span class="sxs-lookup"><span data-stu-id="03ac8-281">Since this function does not refresh file listings or directory display, the calling process should do so upon successful renaming.</span></span>


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> <span data-ttu-id="03ac8-282">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="03ac8-282">WinINet does not support server implementations.</span></span> <span data-ttu-id="03ac8-283">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="03ac8-283">In addition, it should not be used from a service.</span></span> <span data-ttu-id="03ac8-284">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="03ac8-284">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 