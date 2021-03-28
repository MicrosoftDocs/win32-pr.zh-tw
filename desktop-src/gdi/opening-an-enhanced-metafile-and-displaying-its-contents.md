---
description: 本節包含的範例示範應用程式如何開啟儲存在磁片上的增強型中繼檔，以及在工作區中顯示相關聯的圖片。
ms.assetid: e4e5ef5c-d5ea-4931-bbec-1635e8f08c91
title: 開啟增強的中繼檔並顯示其內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f27ce191d66345e5b46ef355757a9c077cf2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972620"
---
# <a name="opening-an-enhanced-metafile-and-displaying-its-contents"></a>開啟增強的中繼檔並顯示其內容

本節包含的範例示範應用程式如何開啟儲存在磁片上的增強型中繼檔，以及在工作區中顯示相關聯的圖片。

此範例會使用 [ **開啟** 一般] 對話方塊，讓使用者從現有的檔案清單中選取增強的中繼檔。 然後，它會將選取之檔案的名稱傳遞至 [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea) 函式，此函式會傳回識別檔案的控制碼。 這個控制碼會傳遞至 [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) 函式，以便顯示圖片。


```C++
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace occurrences of '%' string separator  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
{
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
}
 
LoadString(hInst, IDS_DEFEXTSTRING, 
     (LPSTR)szDefExt, sizeof(szFilter)); 
 
 
// Use the OpenFilename common dialog box  
// to obtain the desired filename.  

szFile[0] = '\0'; 
OPENFILENAME Ofn; 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrCustomFilter = (LPSTR)NULL; 
Ofn.nMaxCustFilter = 0L; 
Ofn.nFilterIndex = 1L; 
Ofn.lpstrFile = szFile; 
Ofn.nMaxFile = sizeof(szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR) NULL; 
Ofn.lpstrTitle = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST; 
Ofn.nFileOffset = 0; 
Ofn.nFileExtension = 0; 
Ofn.lpstrDefExt = szDefExt; 
 
GetOpenFileName(&Ofn); 
 
// Open the metafile.  
 
HENHMETAFILE hemf = GetEnhMetaFile(Ofn.lpstrFile); 
 
// Retrieve a handle to a window device context.  
 
HDC hDC = GetDC(hWnd); 
 
// Retrieve the client rectangle dimensions.  
 
GetClientRect(hWnd, &rct); 
 
// Draw the picture.  
 
PlayEnhMetaFile(hDC, hemf, &rct); 
 
// Release the metafile handle.  
 
DeleteEnhMetaFile(hemf); 
 
// Release the window DC.  
 
ReleaseDC(hWnd, hDC); 
```



 

 



