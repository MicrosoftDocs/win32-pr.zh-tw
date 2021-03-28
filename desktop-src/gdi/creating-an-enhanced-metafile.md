---
description: 本章節包含的範例將示範如何使用使用者指定的檔案名，建立儲存在磁片上的增強型中繼檔。
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: 建立增強型中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4877481ed0a68d6379e7eaabb00bbe37cef74c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512917"
---
# <a name="creating-an-enhanced-metafile"></a><span data-ttu-id="8a768-103">建立增強型中繼檔</span><span class="sxs-lookup"><span data-stu-id="8a768-103">Creating an Enhanced Metafile</span></span>

<span data-ttu-id="8a768-104">本章節包含的範例將示範如何使用使用者指定的檔案名，建立儲存在磁片上的增強型中繼檔。</span><span class="sxs-lookup"><span data-stu-id="8a768-104">This section contains an example that demonstrates the creation of an enhanced metafile that is stored on a disk, using a file name specified by the user.</span></span>

<span data-ttu-id="8a768-105">此範例會使用應用程式視窗的裝置內容作為參考裝置內容。</span><span class="sxs-lookup"><span data-stu-id="8a768-105">The example uses a device context for the application window as the reference device context.</span></span> <span data-ttu-id="8a768-106"> (系統會將此裝置的解析資料儲存在增強型中繼檔的標頭中。 ) 應用程式會藉由呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式，來取得識別此裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8a768-106">(The system stores the resolution data for this device in the enhanced-metafile's header.) The application retrieves a handle identifying this device context by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="8a768-107">此範例會使用應用程式工作區的維度來定義圖片框架的維度。</span><span class="sxs-lookup"><span data-stu-id="8a768-107">The example uses the dimensions of the application's client area to define the dimensions of the picture frame.</span></span> <span data-ttu-id="8a768-108">使用 [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) 函式所傳回的矩形維度，應用程式會將裝置單位轉換成 .01-毫米單位，並將轉換的值傳遞至 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="8a768-108">Using the rectangle dimensions returned by the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function, the application converts the device units to .01-millimeter units and passes the converted values to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="8a768-109">此範例會顯示 [ **另存** 新檔] 對話方塊，讓使用者能夠指定新增強中繼檔的檔案名。</span><span class="sxs-lookup"><span data-stu-id="8a768-109">The example displays a **Save As** common dialog box that enables the user to specify the file name of the new enhanced metafile.</span></span> <span data-ttu-id="8a768-110">系統會將三個字元的 .emf 副檔名附加至這個檔案名，並將名稱傳遞至 [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="8a768-110">The system appends the three-character .emf extension to this file name and passes the name to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="8a768-111">此範例也會在增強型中繼檔標頭中內嵌圖片的文字描述。</span><span class="sxs-lookup"><span data-stu-id="8a768-111">The example also embeds a text description of the picture in the enhanced-metafile header.</span></span> <span data-ttu-id="8a768-112">此描述會在應用程式資源檔的字串資料表中指定為資源。</span><span class="sxs-lookup"><span data-stu-id="8a768-112">This description is specified as a resource in the string table of the application's resource file.</span></span> <span data-ttu-id="8a768-113">不過，在可運作的應用程式中，此字串會從通用對話方塊中的自訂控制項，或從僅針對此用途所顯示的個別對話方塊中取出。</span><span class="sxs-lookup"><span data-stu-id="8a768-113">However, in a working application, this string would be retrieved from a custom control in a common dialog box or from a separate dialog box displayed solely for this purpose.</span></span>


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



 

 
