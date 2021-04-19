---
title: 使用圖示
description: 本節提供的程式碼範例會示範如何執行與圖示相關的工作。
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- 資源，圖示
- 圖示，建立
- 圖示，顯示
- 圖示，共用資源
- 建立圖示
- 顯示圖示
- 共用圖示資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e93f831e3411985ecfb9f841ade750acd4a61b
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/25/2021
ms.locfileid: "106996530"
---
# <a name="using-icons"></a>使用圖示

下列主題說明如何執行與圖示相關的特定工作：

-   [建立圖示](#creating-an-icon)
-   [顯示圖示](#displaying-an-icon)
-   [共用圖示資源](#sharing-icon-resources)

## <a name="creating-an-icon"></a>建立圖示

若要使用圖示，您的應用程式必須取得圖示的控制碼。 下列範例會示範如何建立兩個不同的圖示控點：一個用於標準問題圖示，另一個用於自訂圖示，並在應用程式的資源定義檔中包含為資源。


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



應用程式應該將自訂圖示實作為資源，而且應該使用 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) 或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 函式，而不是在執行時間建立圖示。 這種方法可避免裝置的相依性、簡化當地語系化，以及讓應用程式共用圖示點陣圖。 但是，下列範例會使用 [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) ，在執行時間根據點陣圖位元遮罩建立自訂圖示;其中包含說明系統如何解讀圖示點陣圖位元遮罩。


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



若要建立此圖示， [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) 會將下列事實資料表套用至 AND 和 XOR 位元遮罩。



| 和位元遮罩 | XOR 位元遮罩 | 顯示        |
|-------------|-------------|----------------|
| 0           | 0           | 黑色          |
| 0           | 1           | 白色          |
| 1           | 0           | 畫面         |
| 1           | 1           | 反向畫面 |



 

在關閉之前，您的應用程式必須使用 [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) 來終結使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)所建立的任何圖示。 不需要終結其他函式所建立的圖示。

## <a name="displaying-an-icon"></a>顯示圖示

您的應用程式可以載入並建立圖示，以顯示在應用程式的工作區或子視窗中。 下列範例示範如何在視窗的工作區中繪製圖示，其裝置內容 (DC) 由 *hdc* 參數識別。


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



系統會自動顯示視窗的類別圖示 (s) 。 您的應用程式可以在註冊視窗類別時指派類別圖示。 您的應用程式可以使用 [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) 函數來取代類別圖示。 此函式會變更指定類別之所有視窗的預設視窗設定。 下列範例會將類別圖示取代為其資源識別碼為480的圖示。


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLong(hwnd,          // window handle 
    GCL_HICON,              // changes icon 
    (LONG) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



如需視窗類別的詳細資訊，請參閱 [視窗類別](/windows/desktop/winmsg/window-classes)。

## <a name="sharing-icon-resources"></a>共用圖示資源

下列程式碼會使用 [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)、 [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)和 [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)等函式，以及數個資源函式，根據另一個可執行檔中的圖示資料建立圖示控制碼。 然後，它會在視窗中顯示圖示。

**安全性警告：** 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。 請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
