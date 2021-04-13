---
title: 開啟對話方塊的範例
description: 我們使用的 Shapes 範例有點假設。 讓我們在實際的 Windows 程式中，將開啟的對話方塊轉換成您可以使用的 COM 物件。
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375245"
---
# <a name="example-the-open-dialog-box"></a><span data-ttu-id="55cd2-104">範例：開啟對話方塊</span><span class="sxs-lookup"><span data-stu-id="55cd2-104">Example: The Open Dialog Box</span></span>

<span data-ttu-id="55cd2-105">`Shapes`我們使用的範例有點假設。</span><span class="sxs-lookup"><span data-stu-id="55cd2-105">The `Shapes` example that we have been using is somewhat contrived.</span></span> <span data-ttu-id="55cd2-106">讓我們轉換成您可能在實際 Windows 程式中使用的 COM 物件： [ **開啟** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="55cd2-106">Let's turn to a COM object that you might use in a real Windows program: the **Open** dialog box.</span></span>

![顯示 [開啟] 對話方塊的螢幕擷取畫面](images/fileopen01.png)

<span data-ttu-id="55cd2-108">若要顯示 [ **開啟** ] 對話方塊，程式可以使用稱為 [一般專案] 對話方塊物件的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="55cd2-108">To show the **Open** dialog box, a program can use a COM object called the Common Item Dialog object.</span></span> <span data-ttu-id="55cd2-109">[一般專案] 對話方塊會執行名為 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)的介面，該介面會在標頭檔 shobjidl.h 中宣告。</span><span class="sxs-lookup"><span data-stu-id="55cd2-109">The Common Item Dialog implements an interface named [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), which is declared in the header file Shobjidl.h.</span></span>

<span data-ttu-id="55cd2-110">以下是顯示 [ **開啟** ] 對話方塊給使用者的程式。</span><span class="sxs-lookup"><span data-stu-id="55cd2-110">Here is a program that displays the **Open** dialog box to the user.</span></span> <span data-ttu-id="55cd2-111">如果使用者選取檔案，程式就會顯示包含檔案名的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="55cd2-111">If the user selects a file, the program shows a dialog box that contains the file name.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="55cd2-112">此程式碼會使用稍後將在課程模組中描述的一些概念，如果您不了解這裡的任何內容，請不要擔心。</span><span class="sxs-lookup"><span data-stu-id="55cd2-112">This code uses some concepts that will be described later in the module, so don't worry if you do not understand everything here.</span></span> <span data-ttu-id="55cd2-113">以下是程式碼的基本大綱：</span><span class="sxs-lookup"><span data-stu-id="55cd2-113">Here is a basic outline of the code:</span></span>

1.  <span data-ttu-id="55cd2-114">呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 以初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="55cd2-114">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="55cd2-115">呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立通用專案對話方塊物件，並取得物件之 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="55cd2-115">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Common Item Dialog object and get a pointer to the object's [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span>
3.  <span data-ttu-id="55cd2-116">呼叫物件的 **Show** 方法，該方法會向使用者顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="55cd2-116">Call the object's **Show** method, which shows the dialog box to the user.</span></span> <span data-ttu-id="55cd2-117">這個方法會封鎖，直到使用者關閉對話方塊為止。</span><span class="sxs-lookup"><span data-stu-id="55cd2-117">This method blocks until the user dismisses the dialog box.</span></span>
4.  <span data-ttu-id="55cd2-118">呼叫物件的 [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) 方法。</span><span class="sxs-lookup"><span data-stu-id="55cd2-118">Call the object's [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method.</span></span> <span data-ttu-id="55cd2-119">這個方法會傳回第二個 COM 物件的指標，稱為 *Shell 專案* 物件。</span><span class="sxs-lookup"><span data-stu-id="55cd2-119">This method returns a pointer to a second COM object, called a *Shell item* object.</span></span> <span data-ttu-id="55cd2-120">執行 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 介面的 Shell 專案代表使用者選取的檔案。</span><span class="sxs-lookup"><span data-stu-id="55cd2-120">The Shell item, which implements the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, represents the file that the user selected.</span></span>
5.  <span data-ttu-id="55cd2-121">呼叫 Shell 專案的 [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) 方法。</span><span class="sxs-lookup"><span data-stu-id="55cd2-121">Call the Shell item's [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method.</span></span> <span data-ttu-id="55cd2-122">這個方法會取得檔案路徑（以字串的形式）。</span><span class="sxs-lookup"><span data-stu-id="55cd2-122">This method gets the file path, in the form of a string.</span></span>
6.  <span data-ttu-id="55cd2-123">顯示顯示檔案路徑的訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="55cd2-123">Show a message box that displays the file path.</span></span>
7.  <span data-ttu-id="55cd2-124">呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) 將 COM 程式庫解除初始化。</span><span class="sxs-lookup"><span data-stu-id="55cd2-124">Call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize the COM library.</span></span>

<span data-ttu-id="55cd2-125">COM 程式庫所定義的步驟1、2和7呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="55cd2-125">Steps 1, 2, and 7 call functions that are defined by the COM library.</span></span> <span data-ttu-id="55cd2-126">這些是泛型 COM 函數。</span><span class="sxs-lookup"><span data-stu-id="55cd2-126">These are generic COM functions.</span></span> <span data-ttu-id="55cd2-127">步驟3–5呼叫由通用專案對話方塊物件所定義的方法。</span><span class="sxs-lookup"><span data-stu-id="55cd2-127">Steps 3–5 call methods that are defined by the Common Item Dialog object.</span></span>

<span data-ttu-id="55cd2-128">此範例顯示兩種物件的建立方式：泛型 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函式和方法 ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) 一般專案對話方塊物件特有的) 。</span><span class="sxs-lookup"><span data-stu-id="55cd2-128">This example shows both varieties of object creation: The generic [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, and a method ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) that is specific to the Common Item Dialog object.</span></span>

## <a name="next"></a><span data-ttu-id="55cd2-129">下一個</span><span class="sxs-lookup"><span data-stu-id="55cd2-129">Next</span></span>

[<span data-ttu-id="55cd2-130">管理物件的存留期</span><span class="sxs-lookup"><span data-stu-id="55cd2-130">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a><span data-ttu-id="55cd2-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="55cd2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55cd2-132">開啟對話方塊範例</span><span class="sxs-lookup"><span data-stu-id="55cd2-132">Open Dialog Box Sample</span></span>](open-dialog-box-sample.md)
</dt> </dl>

 

 