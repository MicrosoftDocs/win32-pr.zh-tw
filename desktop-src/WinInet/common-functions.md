---
title: Windows 網際網路) 的一般功能 (
description: 不同的網際網路通訊協定 (例如 ftp 和 HTTP) 會使用數個相同的 WinINet 函數來處理網際網路上的資訊。
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965266"
---
# <a name="common-functions-windows-internet"></a><span data-ttu-id="da314-103">Windows 網際網路) 的一般功能 (</span><span class="sxs-lookup"><span data-stu-id="da314-103">Common Functions (Windows Internet)</span></span>

<span data-ttu-id="da314-104">不同的網際網路通訊協定 (例如 ftp 和 HTTP) 會使用數個相同的 WinINet 函數來處理網際網路上的資訊。</span><span class="sxs-lookup"><span data-stu-id="da314-104">The different Internet protocols (such as ftp and http) use several of the same WinINet functions to handle information on the Internet.</span></span> <span data-ttu-id="da314-105">這些常見的函式會以一致的方式處理其工作，不論所套用的特定通訊協定為何。</span><span class="sxs-lookup"><span data-stu-id="da314-105">These common functions handle their tasks in a consistent manner, regardless of the particular protocol to which they are being applied.</span></span> <span data-ttu-id="da314-106">應用程式可以使用這些函式來建立一般用途的函式，以跨不同的通訊協定處理工作 (例如，讀取 ftp 和 HTTP) 的檔案。</span><span class="sxs-lookup"><span data-stu-id="da314-106">Applications can use these functions to create general-purpose functions that handle tasks across the different protocols (such as reading files for ftp and http).</span></span>

<span data-ttu-id="da314-107">一般函數會處理下列工作：</span><span class="sxs-lookup"><span data-stu-id="da314-107">The common functions handle the following tasks:</span></span>

-   <span data-ttu-id="da314-108">從網際網路下載資源 ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)、 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)和 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)) 。</span><span class="sxs-lookup"><span data-stu-id="da314-108">Downloading resources from the Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), and [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span></span>
-   <span data-ttu-id="da314-109"> ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)) 設定非同步作業。</span><span class="sxs-lookup"><span data-stu-id="da314-109">Setting up asynchronous operations ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span></span>
-   <span data-ttu-id="da314-110"> ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 和 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)) 來查看和變更選項。</span><span class="sxs-lookup"><span data-stu-id="da314-110">Viewing and changing options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span></span>
-   <span data-ttu-id="da314-111">關閉所有類型的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼 ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)) 。</span><span class="sxs-lookup"><span data-stu-id="da314-111">Closing all types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span></span>
-   <span data-ttu-id="da314-112">在資源 ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 和 [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)) 上放置和移除鎖定。</span><span class="sxs-lookup"><span data-stu-id="da314-112">Placing and removing locks on resources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) and [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span></span>

## <a name="using-common-functions"></a><span data-ttu-id="da314-113">使用一般函數</span><span class="sxs-lookup"><span data-stu-id="da314-113">Using Common Functions</span></span>

<span data-ttu-id="da314-114">下表列出 WinINet 函數中包含的一般函數。</span><span class="sxs-lookup"><span data-stu-id="da314-114">The following table lists the common functions included in the WinINet functions.</span></span> <span data-ttu-id="da314-115">一般函數可用於不同類型的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，也可以在不同類型的會話中使用。</span><span class="sxs-lookup"><span data-stu-id="da314-115">The common functions can be used on different types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles or can be used during different types of sessions.</span></span>



| <span data-ttu-id="da314-116">函式</span><span class="sxs-lookup"><span data-stu-id="da314-116">Function</span></span>                                                         | <span data-ttu-id="da314-117">描述</span><span class="sxs-lookup"><span data-stu-id="da314-117">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da314-118">**InternetFindNextFile**</span><span class="sxs-lookup"><span data-stu-id="da314-118">**InternetFindNextFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | <span data-ttu-id="da314-119">繼續進行檔案列舉或搜尋。</span><span class="sxs-lookup"><span data-stu-id="da314-119">Continues file enumeration or search.</span></span> <span data-ttu-id="da314-120">需要 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da314-120">Requires a handle created by the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span>                                                                            |
| [<span data-ttu-id="da314-121">**InternetLockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="da314-121">**InternetLockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | <span data-ttu-id="da314-122">允許使用者將鎖定放置在所使用的檔案上。</span><span class="sxs-lookup"><span data-stu-id="da314-122">Allows the user to place a lock on the file that is being used.</span></span> <span data-ttu-id="da314-123">此函式需要 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da314-123">This function requires a handle returned by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="da314-124">**InternetQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="da314-124">**InternetQueryDataAvailable**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | <span data-ttu-id="da314-125">抓取可用的資料量。</span><span class="sxs-lookup"><span data-stu-id="da314-125">Retrieves the amount of data available.</span></span> <span data-ttu-id="da314-126">需要 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 函數所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da314-126">Requires a handle created by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                                    |
| [<span data-ttu-id="da314-127">**InternetQueryOption**</span><span class="sxs-lookup"><span data-stu-id="da314-127">**InternetQueryOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | <span data-ttu-id="da314-128">抓取網際網路選項的設定。</span><span class="sxs-lookup"><span data-stu-id="da314-128">Retrieves the setting of an Internet option.</span></span>                                                                                                                                                                                                            |
| [<span data-ttu-id="da314-129">**InternetReadFile**</span><span class="sxs-lookup"><span data-stu-id="da314-129">**InternetReadFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | <span data-ttu-id="da314-130">讀取 URL 資料。</span><span class="sxs-lookup"><span data-stu-id="da314-130">Reads URL data.</span></span> <span data-ttu-id="da314-131">需要 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 函數所建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da314-131">Requires a handle created by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                |
| [<span data-ttu-id="da314-132">**InternetSetFilePointer**</span><span class="sxs-lookup"><span data-stu-id="da314-132">**InternetSetFilePointer**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | <span data-ttu-id="da314-133">設定檔案中下一次讀取的位置。</span><span class="sxs-lookup"><span data-stu-id="da314-133">Sets the position for the next read in a file.</span></span> <span data-ttu-id="da314-134">需要以 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (為 HTTP URL 建立的控制碼，) 或使用 GET HTTP 指令動詞 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da314-134">Requires a handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (on an HTTP URL only) or a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) using the GET HTTP verb.</span></span>                 |
| [<span data-ttu-id="da314-135">**InternetSetOption**</span><span class="sxs-lookup"><span data-stu-id="da314-135">**InternetSetOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | <span data-ttu-id="da314-136">設定網際網路選項。</span><span class="sxs-lookup"><span data-stu-id="da314-136">Sets an Internet option.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="da314-137">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="da314-137">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | <span data-ttu-id="da314-138">設定可接收狀態資訊的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="da314-138">Sets a callback function that receives status information.</span></span> <span data-ttu-id="da314-139">將回呼函式指派給指定的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，以及它所衍生的所有控制碼。</span><span class="sxs-lookup"><span data-stu-id="da314-139">Assigns a callback function to the designated [**HINTERNET**](appendix-a-hinternet-handles.md) handle and all handles derived from it.</span></span>                                                      |
| [<span data-ttu-id="da314-140">**InternetUnlockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="da314-140">**InternetUnlockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | <span data-ttu-id="da314-141">解除鎖定使用 [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 函數鎖定的檔案。</span><span class="sxs-lookup"><span data-stu-id="da314-141">Unlocks a file that was locked using the [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function.</span></span>                                                                                                                                           |



 

<span data-ttu-id="da314-142">在支援各種通訊協定和 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼類型的函式中，讀取檔案、尋找下一個檔案、操作選項，以及設定非同步作業，是常見的功能。</span><span class="sxs-lookup"><span data-stu-id="da314-142">Reading files, finding the next file, manipulating options, and setting up asynchronous operations are common to the functions that support various protocols and [**HINTERNET**](appendix-a-hinternet-handles.md) handle types.</span></span>

### <a name="reading-files"></a><span data-ttu-id="da314-143">讀取檔案</span><span class="sxs-lookup"><span data-stu-id="da314-143">Reading Files</span></span>

<span data-ttu-id="da314-144">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)函式是用來從 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函數所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼下載資源。</span><span class="sxs-lookup"><span data-stu-id="da314-144">The [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function is used to download resources from an [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>

<span data-ttu-id="da314-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 接受包含緩衝區位址的 void 指標變數，以及包含緩衝區長度之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="da314-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepts a void pointer variable that contains the address of a buffer and a pointer to a variable that contains the length of the buffer.</span></span> <span data-ttu-id="da314-146">函數會傳回緩衝區中的資料，以及下載到緩衝區的資料量。</span><span class="sxs-lookup"><span data-stu-id="da314-146">The function returns the data in the buffer and the amount of data downloaded into the buffer.</span></span>

<span data-ttu-id="da314-147">WinINet 函數提供兩種方法來下載整個資源：</span><span class="sxs-lookup"><span data-stu-id="da314-147">The WinINet functions provide two techniques to download an entire resource:</span></span>

-   <span data-ttu-id="da314-148">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)函數。</span><span class="sxs-lookup"><span data-stu-id="da314-148">The [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) function.</span></span>
-   <span data-ttu-id="da314-149">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)的傳回值。</span><span class="sxs-lookup"><span data-stu-id="da314-149">The return values of [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>

<span data-ttu-id="da314-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)會採用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 (在控制碼) 上呼叫 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)之後，再傳回可用的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="da314-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) has been called on the handle) and returns the number of bytes available.</span></span> <span data-ttu-id="da314-151">應用程式應配置等於可用位元組數的緩衝區，再加上1代表結束的 **null** 字元，並將該緩衝區與 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="da314-151">The application should allocate a buffer equal to the number of bytes available, plus 1 for the terminating **null** character, and use that buffer with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="da314-152">由於 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) 正在檢查標頭中所列的檔案大小，而不是實際的檔案，因此這個方法不一定會運作。</span><span class="sxs-lookup"><span data-stu-id="da314-152">This method does not always work because [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) is checking the file size listed in the header and not the actual file.</span></span> <span data-ttu-id="da314-153">標頭檔中的資訊可能已過期，或可能遺失標頭檔案，因為並非所有標準都需要此檔案。</span><span class="sxs-lookup"><span data-stu-id="da314-153">The information in the header file could be outdated, or the header file could be missing, since it is not currently required under all standards.</span></span>

<span data-ttu-id="da314-154">下列範例會讀取 hResource 控制碼所存取的資源內容，並顯示在 intCtrlID 所指示的編輯方塊中。</span><span class="sxs-lookup"><span data-stu-id="da314-154">The following example reads the contents of the resource accessed by the hResource handle and displayed in the edit box indicated by intCtrlID.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



<span data-ttu-id="da314-155">當所有可用的資料都已讀取時， [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)會傳回零個位元組的讀取和順利完成。</span><span class="sxs-lookup"><span data-stu-id="da314-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) returns zero bytes read and completes successfully when all available data has been read.</span></span> <span data-ttu-id="da314-156">這可讓應用程式在迴圈中使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 來下載資料，並在傳回0個位元組且成功完成時結束。</span><span class="sxs-lookup"><span data-stu-id="da314-156">This allows an application to use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in a loop to download the data and exit when it returns zero bytes read and completes successfully.</span></span>

<span data-ttu-id="da314-157">下列範例會從網際網路讀取資源，並在 intCtrlID 所指出的編輯方塊中顯示資源。</span><span class="sxs-lookup"><span data-stu-id="da314-157">The following example reads the resource from the Internet and displays the resource in the edit box indicated by intCtrlID.</span></span> <span data-ttu-id="da314-158">[**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 HINTERNET 由 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)) 傳送之後，由 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (傳回。</span><span class="sxs-lookup"><span data-stu-id="da314-158">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hInternet, was returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after being sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span></span>


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a><span data-ttu-id="da314-159">尋找下一個檔案</span><span class="sxs-lookup"><span data-stu-id="da314-159">Finding the Next File</span></span>

<span data-ttu-id="da314-160">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)函式是用來尋找檔案搜尋中的下一個檔案、使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)的搜尋參數和 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼，或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)。</span><span class="sxs-lookup"><span data-stu-id="da314-160">The [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) function is used to find the next file in a file search, using the search parameters and [**HINTERNET**](appendix-a-hinternet-handles.md) handle from [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="da314-161">若要完成檔案搜尋，請繼續使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼來呼叫 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) ，或使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)直到函式失敗，並出現「擴充錯誤訊息 [錯誤」錯誤 \_ \_ \_](wininet-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="da314-161">To complete a file search, continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) using the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) until the function fails with the extended error message [ERROR\_NO\_MORE\_FILES](wininet-errors.md).</span></span> <span data-ttu-id="da314-162">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="da314-162">To get the extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="da314-163">下列範例會在 lstDirectory 所指出的清單方塊中顯示 FTP 目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="da314-163">The following example displays the contents of an FTP directory in the list box indicated by lstDirectory.</span></span> <span data-ttu-id="da314-164">[**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 HConnect 是 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函數在建立 FTP 會話之後所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="da314-164">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hConnect, is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span>


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a><span data-ttu-id="da314-165">操作選項</span><span class="sxs-lookup"><span data-stu-id="da314-165">Manipulating Options</span></span>

<span data-ttu-id="da314-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 和 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 是用來操作 WinINet 選項。</span><span class="sxs-lookup"><span data-stu-id="da314-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) are used to manipulate the WinINet options.</span></span>

<span data-ttu-id="da314-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 接受變數來指出要設定的選項、保存選項設定的緩衝區，以及包含包含緩衝區長度之變數位址的指標。</span><span class="sxs-lookup"><span data-stu-id="da314-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepts a variable that indicates the option to set, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

<span data-ttu-id="da314-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 接受變數來指出要取出的選項、保存選項設定的緩衝區，以及包含包含緩衝區長度之變數位址的指標。</span><span class="sxs-lookup"><span data-stu-id="da314-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepts a variable that indicates the option to retrieve, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

### <a name="setting-up-asynchronous-operations"></a><span data-ttu-id="da314-169">設定非同步作業</span><span class="sxs-lookup"><span data-stu-id="da314-169">Setting Up Asynchronous Operations</span></span>

<span data-ttu-id="da314-170">根據預設，WinINet 函數會以同步方式運作。</span><span class="sxs-lookup"><span data-stu-id="da314-170">By default, the WinINet functions operate synchronously.</span></span> <span data-ttu-id="da314-171">應用程式可以在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)函式的呼叫中設定 [網際網路 \_ 旗標 \_ 非同步](api-flags.md)旗標，以要求非同步作業。</span><span class="sxs-lookup"><span data-stu-id="da314-171">An application can request asynchronous operation by setting the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in the call to the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function.</span></span> <span data-ttu-id="da314-172">針對衍生自 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 所傳回控制碼之控制碼所進行的所有後續呼叫，都會以非同步方式進行。</span><span class="sxs-lookup"><span data-stu-id="da314-172">All future calls made against handles derived from the handle returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) are made asynchronously.</span></span>

<span data-ttu-id="da314-173">非同步與同步作業的原理是讓單一執行緒應用程式能夠充分發揮 CPU 的使用率，而不需要等待網路 i/o 完成。</span><span class="sxs-lookup"><span data-stu-id="da314-173">The rationale for asynchronous versus synchronous operation is to allow a single-threaded application to maximize its utilization of the CPU without having to wait for network I/O to complete.</span></span> <span data-ttu-id="da314-174">因此，視要求而定，作業可能會以同步或非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="da314-174">Therefore, depending on the request, the operation might complete synchronously or asynchronously.</span></span> <span data-ttu-id="da314-175">應用程式應該檢查傳回碼。</span><span class="sxs-lookup"><span data-stu-id="da314-175">The application should check the return code.</span></span> <span data-ttu-id="da314-176">如果函式傳回 **FALSE** 或 **Null**，且 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ IO \_ 暫止，則會以非同步方式發出要求，並在函式完成時，以網際網路 \_ 狀態要求完成來呼叫應用程式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="da314-176">If a function returns **FALSE** or **NULL**, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_IO\_PENDING, the request has been made asynchronously, and the application is called back with INTERNET\_STATUS\_REQUEST\_COMPLETE when the function has completed.</span></span>

<span data-ttu-id="da314-177">若要開始非同步作業，應用程式必須在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)時設定 [網際網路 \_ 旗標 \_ 非同步](api-flags.md)旗標。</span><span class="sxs-lookup"><span data-stu-id="da314-177">To begin asynchronous operation, the application must set the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in its call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="da314-178">然後，應用程式必須使用 [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)註冊有效的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="da314-178">The application must then register a valid callback function, using [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span></span>

<span data-ttu-id="da314-179">為控制碼註冊回呼函數之後，該控制碼上的所有作業都可以產生狀態指標，前提是建立控制碼時所提供的內容值不是零。</span><span class="sxs-lookup"><span data-stu-id="da314-179">After a callback function is registered for a handle, all operations on that handle can generate status indications, provided that the context value that was supplied when the handle was created was not zero.</span></span> <span data-ttu-id="da314-180">提供零內容值會強制作業完成同步，即使在 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)中指定了 [網際網路 \_ 旗標 \_ ASYNC](api-flags.md)也是一樣。</span><span class="sxs-lookup"><span data-stu-id="da314-180">Providing a zero context value forces an operation to complete synchronously, even though [INTERNET\_FLAG\_ASYNC](api-flags.md) was specified in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span>

<span data-ttu-id="da314-181">狀態指示可提供應用程式有關網路作業進度的意見反應，例如解析主機名稱、連接到伺服器，以及接收資料。</span><span class="sxs-lookup"><span data-stu-id="da314-181">Status indications give the application feedback about the progress of network operations, such as resolving a host name, connecting to a server, and receiving data.</span></span> <span data-ttu-id="da314-182">有三個特殊用途的狀態指示可用於控制碼：</span><span class="sxs-lookup"><span data-stu-id="da314-182">Three special-purpose status indications can be made for a handle:</span></span>

-   <span data-ttu-id="da314-183">網際網路 \_ 狀態 \_ 控制碼 \_ 關閉是針對控制碼所做的最後一個狀態指示。</span><span class="sxs-lookup"><span data-stu-id="da314-183">INTERNET\_STATUS\_HANDLE\_CLOSING is the last status indication that is made for a handle.</span></span>
-   <span data-ttu-id="da314-184">\_ \_ 建立的網際網路狀態控制碼 \_ 表示最初建立控制碼的時間。</span><span class="sxs-lookup"><span data-stu-id="da314-184">INTERNET\_STATUS\_HANDLE\_CREATED indicates when the handle is initially created.</span></span>
-   <span data-ttu-id="da314-185">網際網路 \_ 狀態 \_ 要求 \_ 完成表示非同步作業已完成。</span><span class="sxs-lookup"><span data-stu-id="da314-185">INTERNET\_STATUS\_REQUEST\_COMPLETE indicates an asynchronous operation has completed.</span></span>

<span data-ttu-id="da314-186">應用程式必須檢查 [**網際網路 \_ 非同步 \_ 結果**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) 結構，以判斷在收到網際網路 \_ 狀態 \_ 要求完成指示之後，作業是否成功或失敗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="da314-186">The application must check the [**INTERNET\_ASYNC\_RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) structure to determine whether the operation succeeded or failed after receiving an INTERNET\_STATUS\_REQUEST\_COMPLETE indication.</span></span>

<span data-ttu-id="da314-187">下列範例顯示回呼函式的範例，以及呼叫 [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) 以將函式註冊為回呼函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="da314-187">The following sample shows an example of a callback function and a call to [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) to register the function as the callback function.</span></span>


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a><span data-ttu-id="da314-188">關閉 HINTERNET 控制碼</span><span class="sxs-lookup"><span data-stu-id="da314-188">Closing HINTERNET Handles</span></span>

<span data-ttu-id="da314-189">所有的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼都可以使用 [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) 函數來關閉。</span><span class="sxs-lookup"><span data-stu-id="da314-189">All [**HINTERNET**](appendix-a-hinternet-handles.md) handles can be closed by using the [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) function.</span></span> <span data-ttu-id="da314-190">用戶端應用程式必須關閉所有衍生自 **HINTERNET** 控制碼的 **HINTERNET** 控制碼，而這些控制碼是在處理常式上呼叫 [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)之前嘗試關閉的。</span><span class="sxs-lookup"><span data-stu-id="da314-190">Client applications must close all **HINTERNET** handles derived from the **HINTERNET** handle they are trying to close before calling [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle.</span></span>

<span data-ttu-id="da314-191">下列範例說明控制碼階層架構。</span><span class="sxs-lookup"><span data-stu-id="da314-191">The following example illustrates the handle hierarchy.</span></span>


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a><span data-ttu-id="da314-192">鎖定和解除鎖定資源</span><span class="sxs-lookup"><span data-stu-id="da314-192">Locking and Unlocking Resources</span></span>

<span data-ttu-id="da314-193">[**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)函式可讓應用程式確保與傳遞給它的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼相關聯的快取資源不會從快取中消失。</span><span class="sxs-lookup"><span data-stu-id="da314-193">The [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function allows an application to ensure that the cached resource associated with the [**HINTERNET**](appendix-a-hinternet-handles.md) handle passed to it does not disappear from the cache.</span></span> <span data-ttu-id="da314-194">如果另一個下載嘗試認可的資源與鎖定檔案的 URL 相同，則快取會藉由執行安全刪除來避免移除該檔案。</span><span class="sxs-lookup"><span data-stu-id="da314-194">If another download tries to commit a resource that has the same URL as the locked file, the cache avoids removing the file by doing a safe delete.</span></span> <span data-ttu-id="da314-195">在應用程式呼叫 [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) 函式之後，快取會獲得刪除檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="da314-195">After the application calls the [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) function, the cache is given permission to delete the file.</span></span>

<span data-ttu-id="da314-196">如果 [網際網路 \_ 旗標 \_ 沒有 \_ \_](api-flags.md) 快取寫入或 [網際網路旗標尚未 \_ \_ \_](api-flags.md) 設定快取旗標，除非控制碼已連線到 HTTPs 資源，否則 [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 會建立具有副檔名 TMP 的暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="da314-196">If the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) or [INTERNET\_FLAG\_DONT\_CACHE](api-flags.md) flag has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) creates a temporary file with the extension TMP, unless the handle is connected to an https resource.</span></span> <span data-ttu-id="da314-197">如果函式存取 HTTPs 資源和網際網路旗標沒有快取 \_ \_ \_ \_ 寫入 (或網際網路旗標尚未設定快取 \_ \_ \_) ， [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 就會失敗。</span><span class="sxs-lookup"><span data-stu-id="da314-197">If the function accesses an https resource and INTERNET\_FLAG\_NO\_CACHE\_WRITE (or INTERNET\_FLAG\_DONT\_CACHE) has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fails.</span></span>

> [!Note]  
> <span data-ttu-id="da314-198">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="da314-198">WinINet does not support server implementations.</span></span> <span data-ttu-id="da314-199">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="da314-199">In addition, it should not be used from a service.</span></span> <span data-ttu-id="da314-200">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="da314-200">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
