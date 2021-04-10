---
description: 將 Region-Change 支援新增至應用程式
ms.assetid: 4a5c049d-b59f-4130-9252-bc28662a7931
title: 將 Region-Change 支援新增至應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d0bd97bc6249928455ccf9154a91ce2045d8c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187538"
---
# <a name="adding-region-change-support-to-an-application"></a><span data-ttu-id="2fb47-103">將 Region-Change 支援新增至應用程式</span><span class="sxs-lookup"><span data-stu-id="2fb47-103">Adding Region-Change Support to an Application</span></span>

<span data-ttu-id="2fb47-104">下列函式提供給想要將區域變更支援整合至其解碼器或 DVD 應用程式的開發人員。</span><span class="sxs-lookup"><span data-stu-id="2fb47-104">The following functions are provided for developers who wish to integrate region-change support into their decoders or DVD applications.</span></span>


```C++
// Forward declares, constants, typedefs.
const short MAX_DRIVE_NAME = 4;
struct DriveName
{
    TCHAR name[MAX_DRIVE_NAME];
};
BOOL DoesFileExist(LPTSTR pszFile);
BOOL GetDriveLetter(IDvdInfo2 *pDvd, DriveName& szDrive);

#define ARRAY_SIZE(x) (sizeof(x)/sizeof(x[0]))

/////////////////////////////////////////////////////////////////////
// ChangeDVDRegion :  Function to change the DVD drive region.
// Parameters:
//     hWnd - Handle to the application window.
// Returns TRUE if the change is successful, or FALSE otherwise.
// (Failure usually means there was no drive with a valid DVD-V disc.)
/////////////////////////////////////////////////////////////////////
BOOL ChangeDVDRegion(HWND hWnd, IDvdInfo2 *pDvd)
{
    typedef BOOL (APIENTRY *DVDPPLAUNCHER) (HWND hWnd, CHAR DriveLetter);
    
    // First find out which drive is a DVD drive with a valid DVD-V disc.
    DriveName  szDVDDrive;

    if (! GetDriveLetter(pDvd, szDVDDrive) )
    {
        MessageBox(hWnd, TEXT("No DVD drive was found with DVD-V disc."),
            TEXT("Error"), MB_OK | MB_ICONERROR) ;
        return FALSE;
    }

    // Detect the version. 
    
    OSVERSIONINFO   ver;
    ver.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);
    GetVersionEx(&ver);

    if (VER_PLATFORM_WIN32_NT  == ver.dwPlatformId)
    {
        HINSTANCE      hInstDLL;
        DVDPPLAUNCHER  dvdPPLauncher;
        CHAR           szDVDDriveA[MAX_DRIVE_NAME];

        const TCHAR szDllName[] =  TEXT("\\storprop.dll");
        
        // Allocate a large enough string to hold the path + the name.
        TCHAR szCmdLine[MAX_PATH + (sizeof(szDllName)/sizeof(TCHAR)) + 1];

#ifdef UNICODE
        WideCharToMultiByte(CP_ACP, 0, szDVDDrive.name, -1,
            szDVDDriveA, sizeof(szDVDDriveA), NULL, NULL );
#else
        StringCchCopy(szDVDDriveA, MAX_DRIVE_NAME, szDVDDrive.name);
#endif  
        

        UINT cb = GetSystemDirectory(szCmdLine, MAX_PATH + 1);
        if (cb == 0 || cb > MAX_PATH + 1)
        {
            return FALSE;
        }

        StringCchCat(szCmdLine, ARRAY_SIZE(szCmdLine), szDllName);
        
        hInstDLL = LoadLibrary (szCmdLine);
        if (hInstDLL)
        {
            BOOL bResult = FALSE;

            dvdPPLauncher = (DVDPPLAUNCHER) GetProcAddress(hInstDLL,
                "DvdLauncher");
            if (dvdPPLauncher)
            {
                 bResult = dvdPPLauncher(hWnd, szDVDDriveA[0]);
            }
            FreeLibrary(hInstDLL);
            return bResult;
        }
    }  
    else  
    {
        return FALSE;
    }  

    return FALSE;
} 


/////////////////////////////////////////////////////////////////////
// GetDriveLetter: Returns the drive letter of the active DVD drive.
// Parameters:
//     pDvdC - IDvdControl2 interface of the DVD Navigator filter.
//     pszDrive - Receives the first DVD drive with a valid DVD-V disc.
// Returns TRUE if there is a DVD drive with a valid disc.
/////////////////////////////////////////////////////////////////////
BOOL GetDriveLetter(IDvdInfo2 *pDvd, DriveName& pszDrive) 
{
    WCHAR  szPathW[MAX_PATH];
    TCHAR  szPath[MAX_PATH];
    ULONG  ulActualSize = 0;

    pszDrive.name[0] = pszDrive.name[MAX_DRIVE_NAME - 1] = 0;
    
    // Get the current root directory
    HRESULT hr = pDvd->GetDVDDirectory(szPathW, MAX_PATH, &ulActualSize);

    if (SUCCEEDED(hr))
    {

#ifdef UNICODE
        StringCchCopy(pszDrive.name, MAX_DRIVE_NAME, szPathW);
#else
        WideCharToMultiByte(CP_ACP, 0, szPathW, ulActualSize, szPath, MAX_PATH, 0, 0);
        StringCchCopy(pszDrive.name, MAX_DRIVE_NAME, szPath);
#endif  
        
        if (DRIVE_CDROM == GetDriveType(pszDrive.name)) // could be a DVD drive
            return TRUE;
    }

  // Now loop through all the valid drives to detect which one
  // is a DVD drive with a valid DVD-V disc in it.

  // Get all valid drives
  DWORD dwLen = GetLogicalDriveStrings(MAX_PATH, szPath);

  if (dwLen > MAX_PATH)
  {
      // The function returns a larger value if the buffer is too small.
      return FALSE;
  }

  // Try all drives one by one
  for (size_t dw = 0; dw < dwLen; ) 
  {
      
      TCHAR *szTmp = szPath + dw;
      
      // Look only for CD-ROM drives that has a disc with required (.ifo) files
      if (DRIVE_CDROM  == GetDriveType(szTmp)) 
      {
          TCHAR   szDVDPath1[MAX_PATH + 1];
          TCHAR   szDVDPath2[MAX_PATH + 1];
          
          StringCchCopy(szDVDPath1, MAX_DRIVE_NAME, szTmp);
          StringCchCopy(szDVDPath2, MAX_DRIVE_NAME, szTmp);
          StringCchCat(szDVDPath1, ARRAY_SIZE(szDVDPath1), TEXT("Video_ts\\Video_ts.ifo"));
          StringCchCat(szDVDPath2, ARRAY_SIZE(szDVDPath2), TEXT("Video_ts\\Vts_01_0.ifo"));
          
          // If the .ifo files exist on this drive then it has a valid DVD-V disc
          if (DoesFileExist(szDVDPath1) && DoesFileExist(szDVDPath2))    
          {
              StringCchCopy(pszDrive.name, MAX_DRIVE_NAME, szTmp);
              return TRUE;   // return the first drive that has a valid DVD-V disc
          }
      }

      size_t len = 0;
      StringCchLength(szTmp, STRSAFE_MAX_CCH, &len);
      dw += len + 1;
  }

  return FALSE ;   // didn't find any DVD drive with DVD-V content
} 

/////////////////////////////////////////////////////////////////////
// DoesFileExist : Determines whether a specified file exists
// Parameters:
//     pszFile - File name to check.
// Returns TRUE if the specified file is found, or FALSE otherwise.
/////////////////////////////////////////////////////////////////////
BOOL DoesFileExist(LPTSTR pszFile)
{
    if (pszFile == NULL)
    {
        return FALSE;
    }

    size_t len = 0;

    if (FAILED(StringCchLength(pszFile, STRSAFE_MAX_CCH, &len)))
    {
        return FALSE;
    }

    if (len > MAX_PATH)
    {
        return FALSE;
    }


    // We don't want any error message box to pop up when we try to test
    // if the required file is available to open for read --apcb.
    
    UINT uErrorMode = SetErrorMode(SEM_FAILCRITICALERRORS | SEM_NOOPENFILEERRORBOX);
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, FILE_SHARE_READ, NULL, 
        OPEN_EXISTING, FILE_FLAG_SEQUENTIAL_SCAN, NULL);

    SetErrorMode(uErrorMode);  // restore error mode
    
    if (INVALID_HANDLE_VALUE  == hFile) 
    {
        return FALSE;    
    }
    
    CloseHandle(hFile);
    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="2fb47-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="2fb47-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb47-106">Windows 中的 DVD 區域變更支援</span><span class="sxs-lookup"><span data-stu-id="2fb47-106">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



