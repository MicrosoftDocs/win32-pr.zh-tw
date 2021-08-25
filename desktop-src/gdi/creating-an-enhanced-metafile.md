---
description: 本章節包含的範例將示範如何使用使用者指定的檔案名，建立儲存在磁片上的增強型中繼檔。
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: 建立增強型中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e53266ac0677da211308c7028f4d61869fc2890f27c06daeff9cfb6fea87e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849228"
---
# <a name="creating-an-enhanced-metafile"></a>建立增強型中繼檔

本章節包含的範例將示範如何使用使用者指定的檔案名，建立儲存在磁片上的增強型中繼檔。

此範例會使用應用程式視窗的裝置內容作為參考裝置內容。  (系統會將此裝置的解析資料儲存在增強型中繼檔的標頭中。 ) 應用程式會藉由呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式，來取得識別此裝置內容的控制碼。

此範例會使用應用程式工作區的維度來定義圖片框架的維度。 使用 [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) 函式所傳回的矩形維度，應用程式會將裝置單位轉換成 .01-毫米單位，並將轉換的值傳遞至 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) 函式。

此範例會顯示 [ **另存** 新檔] 對話方塊，讓使用者能夠指定新增強中繼檔的檔案名。 系統會將三個字元的 .emf 副檔名附加至這個檔案名，並將名稱傳遞至 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) 函式。

此範例也會在增強型中繼檔標頭中內嵌圖片的文字描述。 此描述會在應用程式資源檔的字串資料表中指定為資源。 不過，在可運作的應用程式中，此字串會從通用對話方塊中的自訂控制項，或從僅針對此用途所顯示的個別對話方塊中取出。


```C++
// Obtain a handle to a reference device context.  
 
hdcRef = GetDC(hWnd); 
 
// Determine the picture frame dimensions.  
// iWidthMM is the display width in millimeters.  
// iHeightMM is the display height in millimeters.  
// iWidthPels is the display width in pixels.  
// iHeightPels is the display height in pixels  
 
iWidthMM = GetDeviceCaps(hdcRef, HORZSIZE); 
iHeightMM = GetDeviceCaps(hdcRef, VERTSIZE); 
iWidthPels = GetDeviceCaps(hdcRef, HORZRES); 
iHeightPels = GetDeviceCaps(hdcRef, VERTRES); 
 
// Retrieve the coordinates of the client  
// rectangle, in pixels.  
 
GetClientRect(hWnd, &rect); 
 
// Convert client coordinates to .01-mm units.  
// Use iWidthMM, iWidthPels, iHeightMM, and  
// iHeightPels to determine the number of  
// .01-millimeter units per pixel in the x-  
//  and y-directions.  
 
rect.left = (rect.left * iWidthMM * 100)/iWidthPels; 
rect.top = (rect.top * iHeightMM * 100)/iHeightPels; 
rect.right = (rect.right * iWidthMM * 100)/iWidthPels; 
rect.bottom = (rect.bottom * iHeightMM * 100)/iHeightPels; 
 
// Load the filename filter from the string table.  
 
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace the '%' separators that are embedded  
// between the strings in the string-table entry  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
 
// Load the dialog title string from the table.  
 
LoadString(hInst, IDS_TITLESTRING, 
     (LPSTR)szTitle, sizeof(szTitle)); 
 
// Initialize the OPENFILENAME members.  
 
szFile[0] = '\0'; 
 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrFile= szFile; 
Ofn.nMaxFile = sizeof(szFile)/ sizeof(*szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_OVERWRITEPROMPT; 
Ofn.lpstrTitle = szTitle; 
 
// Display the Filename common dialog box. The  
// filename specified by the user is passed  
// to the CreateEnhMetaFile function and used to  
// store the metafile on disk.  
 
GetSaveFileName(&Ofn); 
 
// Load the description from the string table.  
 
LoadString(hInst, IDS_DESCRIPTIONSTRING, 
     (LPSTR)szDescription, sizeof(szDescription)); 
 
// Replace the '%' string separators that are  
// embedded between strings in the string-table  
// entry with '\0'.  
 
for (i=0; szDescription[i]!='\0'; i++) 
{
    if (szDescription[i] == '%') 
            szDescription[i] = '\0'; 
}
 
// Create the metafile device context.  
 
hdcMeta = CreateEnhMetaFile(hdcRef, 
          (LPTSTR) Ofn.lpstrFile, 
          &rect, (LPSTR)szDescription); 
 
if (!hdcMeta) 
    errhandler("CreateEnhMetaFile", hWnd); 
 
// Release the reference device context.  
 
ReleaseDC(hWnd, hdcRef); 
```



 

 
