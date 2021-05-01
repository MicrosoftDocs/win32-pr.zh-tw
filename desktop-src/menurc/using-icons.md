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
ms.openlocfilehash: 03202c250502794d5f845bcc8c2ae263d919ea62
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327113"
---
# <a name="using-icons"></a><span data-ttu-id="78d1f-110">使用圖示</span><span class="sxs-lookup"><span data-stu-id="78d1f-110">Using Icons</span></span>

<span data-ttu-id="78d1f-111">下列主題說明如何執行與圖示相關的特定工作：</span><span class="sxs-lookup"><span data-stu-id="78d1f-111">The following topics describe how to perform certain tasks related to icons:</span></span>

-   [<span data-ttu-id="78d1f-112">建立圖示</span><span class="sxs-lookup"><span data-stu-id="78d1f-112">Creating an Icon</span></span>](#creating-an-icon)
-   [<span data-ttu-id="78d1f-113">顯示圖示</span><span class="sxs-lookup"><span data-stu-id="78d1f-113">Displaying an Icon</span></span>](#displaying-an-icon)
-   [<span data-ttu-id="78d1f-114">共用圖示資源</span><span class="sxs-lookup"><span data-stu-id="78d1f-114">Sharing Icon Resources</span></span>](#sharing-icon-resources)

## <a name="creating-an-icon"></a><span data-ttu-id="78d1f-115">建立圖示</span><span class="sxs-lookup"><span data-stu-id="78d1f-115">Creating an Icon</span></span>

<span data-ttu-id="78d1f-116">若要使用圖示，您的應用程式必須取得圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="78d1f-116">To use an icon, your application must get a handle to the icon.</span></span> <span data-ttu-id="78d1f-117">下列範例會示範如何建立兩個不同的圖示控點：一個用於標準問題圖示，另一個用於自訂圖示，並在應用程式的資源定義檔中包含為資源。</span><span class="sxs-lookup"><span data-stu-id="78d1f-117">The following example shows how to create two different icon handles: one for the standard question icon and one for a custom icon included as a resource in the application's resource-definition file.</span></span>


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



<span data-ttu-id="78d1f-118">應用程式應該將自訂圖示實作為資源，而且應該使用 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) 或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 函式，而不是在執行時間建立圖示。</span><span class="sxs-lookup"><span data-stu-id="78d1f-118">An application should implement custom icons as resources and should use the [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function, rather than create the icons at run-time.</span></span> <span data-ttu-id="78d1f-119">這種方法可避免裝置的相依性、簡化當地語系化，以及讓應用程式共用圖示點陣圖。</span><span class="sxs-lookup"><span data-stu-id="78d1f-119">This approach avoids device dependence, simplifies localization, and enables applications to share icon bitmaps.</span></span> <span data-ttu-id="78d1f-120">但是，下列範例會使用 [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) ，在執行時間根據點陣圖位元遮罩建立自訂圖示;其中包含說明系統如何解讀圖示點陣圖位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="78d1f-120">However, the following example uses [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) to create a custom icon at run-time, based on bitmap bitmasks; it is included to illustrate how the system interprets icon bitmap bitmasks.</span></span>


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



<span data-ttu-id="78d1f-121">若要建立此圖示， [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) 會將下列事實資料表套用至 AND 和 XOR 位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="78d1f-121">To create the icon, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applies the following truth table to the AND and XOR bitmasks.</span></span>



| <span data-ttu-id="78d1f-122">和位元遮罩</span><span class="sxs-lookup"><span data-stu-id="78d1f-122">AND bitmask</span></span> | <span data-ttu-id="78d1f-123">XOR 位元遮罩</span><span class="sxs-lookup"><span data-stu-id="78d1f-123">XOR bitmask</span></span> | <span data-ttu-id="78d1f-124">顯示</span><span class="sxs-lookup"><span data-stu-id="78d1f-124">Display</span></span>        |
|-------------|-------------|----------------|
| <span data-ttu-id="78d1f-125">0</span><span class="sxs-lookup"><span data-stu-id="78d1f-125">0</span></span>           | <span data-ttu-id="78d1f-126">0</span><span class="sxs-lookup"><span data-stu-id="78d1f-126">0</span></span>           | <span data-ttu-id="78d1f-127">黑色</span><span class="sxs-lookup"><span data-stu-id="78d1f-127">Black</span></span>          |
| <span data-ttu-id="78d1f-128">0</span><span class="sxs-lookup"><span data-stu-id="78d1f-128">0</span></span>           | <span data-ttu-id="78d1f-129">1</span><span class="sxs-lookup"><span data-stu-id="78d1f-129">1</span></span>           | <span data-ttu-id="78d1f-130">白色</span><span class="sxs-lookup"><span data-stu-id="78d1f-130">White</span></span>          |
| <span data-ttu-id="78d1f-131">1</span><span class="sxs-lookup"><span data-stu-id="78d1f-131">1</span></span>           | <span data-ttu-id="78d1f-132">0</span><span class="sxs-lookup"><span data-stu-id="78d1f-132">0</span></span>           | <span data-ttu-id="78d1f-133">畫面</span><span class="sxs-lookup"><span data-stu-id="78d1f-133">Screen</span></span>         |
| <span data-ttu-id="78d1f-134">1</span><span class="sxs-lookup"><span data-stu-id="78d1f-134">1</span></span>           | <span data-ttu-id="78d1f-135">1</span><span class="sxs-lookup"><span data-stu-id="78d1f-135">1</span></span>           | <span data-ttu-id="78d1f-136">反向畫面</span><span class="sxs-lookup"><span data-stu-id="78d1f-136">Reverse screen</span></span> |



 

<span data-ttu-id="78d1f-137">在關閉之前，您的應用程式必須使用 [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) 來終結使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)所建立的任何圖示。</span><span class="sxs-lookup"><span data-stu-id="78d1f-137">Before closing, your application must use [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) to destroy any icon it created by using [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span></span> <span data-ttu-id="78d1f-138">不需要終結其他函式所建立的圖示。</span><span class="sxs-lookup"><span data-stu-id="78d1f-138">It is not necessary to destroy icons created by other functions.</span></span>

## <a name="displaying-an-icon"></a><span data-ttu-id="78d1f-139">顯示圖示</span><span class="sxs-lookup"><span data-stu-id="78d1f-139">Displaying an Icon</span></span>

<span data-ttu-id="78d1f-140">您的應用程式可以載入並建立圖示，以顯示在應用程式的工作區或子視窗中。</span><span class="sxs-lookup"><span data-stu-id="78d1f-140">Your application can load and create icons to display in the application's client area or child windows.</span></span> <span data-ttu-id="78d1f-141">下列範例示範如何在視窗的工作區中繪製圖示，其裝置內容 (DC) 由 *hdc* 參數識別。</span><span class="sxs-lookup"><span data-stu-id="78d1f-141">The following example demonstrates how to draw an icon in the client area of the window whose device context (DC) is identified by the *hdc* parameter.</span></span>


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



<span data-ttu-id="78d1f-142">系統會自動顯示視窗的類別圖示 (s) 。</span><span class="sxs-lookup"><span data-stu-id="78d1f-142">The system automatically displays the class icon(s) for a window.</span></span> <span data-ttu-id="78d1f-143">您的應用程式可以在註冊視窗類別時指派類別圖示。</span><span class="sxs-lookup"><span data-stu-id="78d1f-143">Your application can assign class icons while registering a window class.</span></span> <span data-ttu-id="78d1f-144">您的應用程式可以使用 [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) 函數來取代類別圖示。</span><span class="sxs-lookup"><span data-stu-id="78d1f-144">Your application can replace a class icon by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="78d1f-145">此函式會變更指定類別之所有視窗的預設視窗設定。</span><span class="sxs-lookup"><span data-stu-id="78d1f-145">This function changes the default window settings for all windows of a given class.</span></span> <span data-ttu-id="78d1f-146">下列範例會將類別圖示取代為其資源識別碼為480的圖示。</span><span class="sxs-lookup"><span data-stu-id="78d1f-146">The following example replaces a class icon with the icon whose resource identifier is 480.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



<span data-ttu-id="78d1f-147">如需視窗類別的詳細資訊，請參閱 [視窗類別](/windows/desktop/winmsg/window-classes)。</span><span class="sxs-lookup"><span data-stu-id="78d1f-147">For more information about window classes, see [Window Classes](/windows/desktop/winmsg/window-classes).</span></span>

## <a name="sharing-icon-resources"></a><span data-ttu-id="78d1f-148">共用圖示資源</span><span class="sxs-lookup"><span data-stu-id="78d1f-148">Sharing Icon Resources</span></span>

<span data-ttu-id="78d1f-149">下列程式碼會使用 [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)、 [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)和 [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)等函式，以及數個資源函式，根據另一個可執行檔中的圖示資料建立圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="78d1f-149">The following code uses the functions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), and [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), and several of the resource functions, to create an icon handle based on icon data from another executable file.</span></span> <span data-ttu-id="78d1f-150">然後，它會在視窗中顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="78d1f-150">Then, it displays the icon in a window.</span></span>

<span data-ttu-id="78d1f-151">**安全性警告：** 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="78d1f-151">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="78d1f-152">請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78d1f-152">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


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



 

 
