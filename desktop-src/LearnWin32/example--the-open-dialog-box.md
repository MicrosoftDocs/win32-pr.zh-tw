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
# <a name="example-the-open-dialog-box"></a>範例：開啟對話方塊

`Shapes`我們使用的範例有點假設。 讓我們轉換成您可能在實際 Windows 程式中使用的 COM 物件： [ **開啟** ] 對話方塊。

![顯示 [開啟] 對話方塊的螢幕擷取畫面](images/fileopen01.png)

若要顯示 [ **開啟** ] 對話方塊，程式可以使用稱為 [一般專案] 對話方塊物件的 COM 物件。 [一般專案] 對話方塊會執行名為 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)的介面，該介面會在標頭檔 shobjidl.h 中宣告。

以下是顯示 [ **開啟** ] 對話方塊給使用者的程式。 如果使用者選取檔案，程式就會顯示包含檔案名的對話方塊。


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



此程式碼會使用稍後將在課程模組中描述的一些概念，如果您不了解這裡的任何內容，請不要擔心。 以下是程式碼的基本大綱：

1.  呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 以初始化 COM 程式庫。
2.  呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立通用專案對話方塊物件，並取得物件之 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面的指標。
3.  呼叫物件的 **Show** 方法，該方法會向使用者顯示對話方塊。 這個方法會封鎖，直到使用者關閉對話方塊為止。
4.  呼叫物件的 [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) 方法。 這個方法會傳回第二個 COM 物件的指標，稱為 *Shell 專案* 物件。 執行 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 介面的 Shell 專案代表使用者選取的檔案。
5.  呼叫 Shell 專案的 [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) 方法。 這個方法會取得檔案路徑（以字串的形式）。
6.  顯示顯示檔案路徑的訊息方塊。
7.  呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) 將 COM 程式庫解除初始化。

COM 程式庫所定義的步驟1、2和7呼叫函式。 這些是泛型 COM 函數。 步驟3–5呼叫由通用專案對話方塊物件所定義的方法。

此範例顯示兩種物件的建立方式：泛型 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函式和方法 ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) 一般專案對話方塊物件特有的) 。

## <a name="next"></a>下一個

[管理物件的存留期](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開啟對話方塊範例](open-dialog-box-sample.md)
</dt> </dl>

 

 