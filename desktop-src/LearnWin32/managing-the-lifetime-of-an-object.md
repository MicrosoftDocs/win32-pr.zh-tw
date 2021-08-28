---
title: 管理物件的存留期
description: 瞭解如何管理 AddRef 和發行方法，以控制物件的存留期。
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a10ec4e7a873c5e8b86c3d2bfe91fd1531051d599831151d3dbec5ed3d70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897424"
---
# <a name="managing-the-lifetime-of-an-object"></a>管理物件的存留期

我們尚未提及的 COM 介面有一個規則。 每個 COM 介面都必須直接或間接繼承自名為 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)的介面。 這個介面會提供所有 COM 物件都必須支援的一些基本功能。

[**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面會定義三個方法：

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**釋放**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法可讓程式在執行時間查詢物件的功能。 在下一個主題中，我們將詳細說明如何 [針對介面提出物件](asking-an-object-for-an-interface.md)。 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)方法是用來控制物件的存留期。 這是本主題的主題。

## <a name="reference-counting"></a>參考計數

程式可能會做的任何事，在某個時間點會配置和釋出資源。 配置資源很簡單。 知道何時釋出資源很困難，特別是當資源的存留期超出目前範圍時。 這個問題對 COM 而言並不是唯一的。 配置堆積記憶體的任何程式都必須解決相同的問題。 例如，c + + 會使用自動析構函數，而 c # 和 JAVA 則使用垃圾收集。 COM 使用稱為 *參考計數* 的方法。

每個 COM 物件都會維護內部計數。 這就是所謂的參考計數。 參考計數會追蹤目前作用中物件的參考數目。 當參考的數目降至零時，物件就會刪除本身。 最後一個部分值得重複：物件會刪除本身。 程式永遠不會明確刪除物件。

以下是參考計數的規則：

-   第一次建立物件時，它的參考計數為1。 此時，程式具有物件的單一指標。
-   程式可以複製 (複製) 指標來建立新的參考。 當您複製指標時，您必須呼叫物件的 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 方法。 這個方法會將參考計數遞增一。
-   當您完成使用物件的指標時，您必須呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)。 **發行** 方法會將參考計數遞減一。 它也會使指標失效。 呼叫 **Release** 之後，請不要再使用指標。  (如果您有相同物件的其他指標，您可以繼續使用這些指標。 ) 
-   當您使用每個指標呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 時，物件的物件參考計數會到達零，而物件會刪除本身。

下圖顯示簡單但一般的案例。

![顯示簡單參考計數案例的圖表。](images/com04.png)

此程式會建立物件，並將指標 (*p*) 儲存至物件。 此時，參考計數為1。 當程式完成使用指標時，它會呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)。 參考計數會減少為零，而物件會刪除本身。 現在 *p* 是不正確。 將 *p* 用於任何進一步的方法呼叫時，會發生錯誤。

下圖顯示更複雜的範例。

![顯示參考計數的圖例](images/com05.png)

在這裡，程式會建立物件，並將指標 *p* 儲存在前面。 接下來，程式會將 *p* 複製到新的變數 *q*。 此時，程式必須呼叫 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 來遞增參考計數。 參考計數現在是2，而物件有兩個有效的指標。 現在假設程式已使用 *p* 完成。 此程式會呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)，參考計數會變成1，而 *p* 不再有效。 但 *q* 仍有效。 之後，程式就會使用 *q* 完成。 因此，它會再次呼叫 **發行** 。 參考計數會變成零，而物件會刪除本身。

您可能會想知道程式會複製 *p* 的原因。 有兩個主要的原因：首先，您可能會想要將指標儲存在資料結構中，例如清單。 其次，您可能會想要將指標保持在原始變數的目前範圍之外。 因此，您可以將它複製到範圍較廣的新變數。

參考計數的其中一個優點是您可以在不同的程式碼區段之間共用指標，而不需要針對不同的程式碼路徑進行協調來刪除物件。 相反地，每個程式碼路徑只會在該程式碼路徑使用物件完成時，呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。 物件會在正確的時間處理本身的刪除。

## <a name="example"></a>範例

以下是再次 [開啟對話方塊範例](example--the-open-dialog-box.md) 中的程式碼。

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

參考計數會在此程式碼的兩個位置進行。 首先，如果程式成功建立一般專案對話方塊物件，它必須在 *pFileOpen* 指標上呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

其次，當 [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)方法傳回 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)介面的指標時，程式必須在 *pItem* 指標上呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

請注意，在這兩種情況下， [**釋放**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 呼叫是指標超出範圍之前所發生的最後一件事。 另外也請注意，只有在您測試 **HRESULT** 是否成功之後，才會呼叫此 **版本**。 例如，如果對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 的呼叫失敗， *pFileOpen* 指標就會無效。 因此，在指標上呼叫 **Release** 會是錯誤。

## <a name="next"></a>下一個

[要求物件提供介面](asking-an-object-for-an-interface.md)