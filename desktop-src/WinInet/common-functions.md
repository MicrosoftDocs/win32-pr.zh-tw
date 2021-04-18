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
# <a name="common-functions-windows-internet"></a>Windows 網際網路) 的一般功能 (

不同的網際網路通訊協定 (例如 ftp 和 HTTP) 會使用數個相同的 WinINet 函數來處理網際網路上的資訊。 這些常見的函式會以一致的方式處理其工作，不論所套用的特定通訊協定為何。 應用程式可以使用這些函式來建立一般用途的函式，以跨不同的通訊協定處理工作 (例如，讀取 ftp 和 HTTP) 的檔案。

一般函數會處理下列工作：

-   從網際網路下載資源 ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)、 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)和 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)) 。
-    ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)) 設定非同步作業。
-    ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 和 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)) 來查看和變更選項。
-   關閉所有類型的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼 ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)) 。
-   在資源 ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 和 [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)) 上放置和移除鎖定。

## <a name="using-common-functions"></a>使用一般函數

下表列出 WinINet 函數中包含的一般函數。 一般函數可用於不同類型的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，也可以在不同類型的會話中使用。



| 函式                                                         | 描述                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | 繼續進行檔案列舉或搜尋。 需要 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數所建立的控制碼。                                                                            |
| [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | 允許使用者將鎖定放置在所使用的檔案上。 此函式需要 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數所傳回的控制碼。 |
| [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | 抓取可用的資料量。 需要 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 函數所建立的控制碼。                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | 抓取網際網路選項的設定。                                                                                                                                                                                                            |
| [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | 讀取 URL 資料。 需要 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 函數所建立的控制碼。                                                                |
| [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | 設定檔案中下一次讀取的位置。 需要以 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (為 HTTP URL 建立的控制碼，) 或使用 GET HTTP 指令動詞 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) 建立的控制碼。                 |
| [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | 設定網際網路選項。                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | 設定可接收狀態資訊的回呼函數。 將回呼函式指派給指定的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，以及它所衍生的所有控制碼。                                                      |
| [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | 解除鎖定使用 [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 函數鎖定的檔案。                                                                                                                                           |



 

在支援各種通訊協定和 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼類型的函式中，讀取檔案、尋找下一個檔案、操作選項，以及設定非同步作業，是常見的功能。

### <a name="reading-files"></a>讀取檔案

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)函式是用來從 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函數所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼下載資源。

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 接受包含緩衝區位址的 void 指標變數，以及包含緩衝區長度之變數的指標。 函數會傳回緩衝區中的資料，以及下載到緩衝區的資料量。

WinINet 函數提供兩種方法來下載整個資源：

-   [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)函數。
-   [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)的傳回值。

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)會採用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 (在控制碼) 上呼叫 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)之後，再傳回可用的位元組數目。 應用程式應配置等於可用位元組數的緩衝區，再加上1代表結束的 **null** 字元，並將該緩衝區與 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)搭配使用。 由於 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) 正在檢查標頭中所列的檔案大小，而不是實際的檔案，因此這個方法不一定會運作。 標頭檔中的資訊可能已過期，或可能遺失標頭檔案，因為並非所有標準都需要此檔案。

下列範例會讀取 hResource 控制碼所存取的資源內容，並顯示在 intCtrlID 所指示的編輯方塊中。


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



當所有可用的資料都已讀取時， [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)會傳回零個位元組的讀取和順利完成。 這可讓應用程式在迴圈中使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 來下載資料，並在傳回0個位元組且成功完成時結束。

下列範例會從網際網路讀取資源，並在 intCtrlID 所指出的編輯方塊中顯示資源。 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 HINTERNET 由 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)) 傳送之後，由 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)或 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (傳回。


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



### <a name="finding-the-next-file"></a>尋找下一個檔案

[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)函式是用來尋找檔案搜尋中的下一個檔案、使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)的搜尋參數和 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼，或 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)。

若要完成檔案搜尋，請繼續使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼來呼叫 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) ，或使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)直到函式失敗，並出現「擴充錯誤訊息 [錯誤」錯誤 \_ \_ \_](wininet-errors.md)。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

下列範例會在 lstDirectory 所指出的清單方塊中顯示 FTP 目錄的內容。 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼 HConnect 是 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函數在建立 FTP 會話之後所傳回的控制碼。


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



### <a name="manipulating-options"></a>操作選項

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 和 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 是用來操作 WinINet 選項。

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 接受變數來指出要設定的選項、保存選項設定的緩衝區，以及包含包含緩衝區長度之變數位址的指標。

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 接受變數來指出要取出的選項、保存選項設定的緩衝區，以及包含包含緩衝區長度之變數位址的指標。

### <a name="setting-up-asynchronous-operations"></a>設定非同步作業

根據預設，WinINet 函數會以同步方式運作。 應用程式可以在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)函式的呼叫中設定 [網際網路 \_ 旗標 \_ 非同步](api-flags.md)旗標，以要求非同步作業。 針對衍生自 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 所傳回控制碼之控制碼所進行的所有後續呼叫，都會以非同步方式進行。

非同步與同步作業的原理是讓單一執行緒應用程式能夠充分發揮 CPU 的使用率，而不需要等待網路 i/o 完成。 因此，視要求而定，作業可能會以同步或非同步方式完成。 應用程式應該檢查傳回碼。 如果函式傳回 **FALSE** 或 **Null**，且 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ IO \_ 暫止，則會以非同步方式發出要求，並在函式完成時，以網際網路 \_ 狀態要求完成來呼叫應用程式 \_ \_ 。

若要開始非同步作業，應用程式必須在呼叫 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)時設定 [網際網路 \_ 旗標 \_ 非同步](api-flags.md)旗標。 然後，應用程式必須使用 [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)註冊有效的回呼函數。

為控制碼註冊回呼函數之後，該控制碼上的所有作業都可以產生狀態指標，前提是建立控制碼時所提供的內容值不是零。 提供零內容值會強制作業完成同步，即使在 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)中指定了 [網際網路 \_ 旗標 \_ ASYNC](api-flags.md)也是一樣。

狀態指示可提供應用程式有關網路作業進度的意見反應，例如解析主機名稱、連接到伺服器，以及接收資料。 有三個特殊用途的狀態指示可用於控制碼：

-   網際網路 \_ 狀態 \_ 控制碼 \_ 關閉是針對控制碼所做的最後一個狀態指示。
-   \_ \_ 建立的網際網路狀態控制碼 \_ 表示最初建立控制碼的時間。
-   網際網路 \_ 狀態 \_ 要求 \_ 完成表示非同步作業已完成。

應用程式必須檢查 [**網際網路 \_ 非同步 \_ 結果**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) 結構，以判斷在收到網際網路 \_ 狀態 \_ 要求完成指示之後，作業是否成功或失敗 \_ 。

下列範例顯示回呼函式的範例，以及呼叫 [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) 以將函式註冊為回呼函式的呼叫。


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



### <a name="closing-hinternet-handles"></a>關閉 HINTERNET 控制碼

所有的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼都可以使用 [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) 函數來關閉。 用戶端應用程式必須關閉所有衍生自 **HINTERNET** 控制碼的 **HINTERNET** 控制碼，而這些控制碼是在處理常式上呼叫 [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)之前嘗試關閉的。

下列範例說明控制碼階層架構。


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



### <a name="locking-and-unlocking-resources"></a>鎖定和解除鎖定資源

[**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)函式可讓應用程式確保與傳遞給它的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼相關聯的快取資源不會從快取中消失。 如果另一個下載嘗試認可的資源與鎖定檔案的 URL 相同，則快取會藉由執行安全刪除來避免移除該檔案。 在應用程式呼叫 [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) 函式之後，快取會獲得刪除檔案的許可權。

如果 [網際網路 \_ 旗標 \_ 沒有 \_ \_](api-flags.md) 快取寫入或 [網際網路旗標尚未 \_ \_ \_](api-flags.md) 設定快取旗標，除非控制碼已連線到 HTTPs 資源，否則 [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 會建立具有副檔名 TMP 的暫存檔案。 如果函式存取 HTTPs 資源和網際網路旗標沒有快取 \_ \_ \_ \_ 寫入 (或網際網路旗標尚未設定快取 \_ \_ \_) ， [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) 就會失敗。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 
