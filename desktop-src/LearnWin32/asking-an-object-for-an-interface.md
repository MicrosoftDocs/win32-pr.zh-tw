---
title: 要求物件提供介面
description: 要求物件提供介面
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023485"
---
# <a name="asking-an-object-for-an-interface"></a>要求物件提供介面

我們稍早看到某個物件可以執行多個介面。 一般專案對話方塊物件是這個的真實世界範例。 為了支援最常見的用法，此物件會實 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面。 此介面會定義用來顯示對話方塊以及取得所選檔案相關資訊的基本方法。 不過，若要使用更先進的用法，此物件也會實作為一個名為 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)的介面。 程式可以使用此介面，藉由加入新的 UI 控制項來自訂對話方塊的外觀和行為。

回想一下，每個 COM 介面都必須直接或間接繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面。 下圖顯示 [一般專案] 對話方塊物件的繼承。

![顯示通用專案對話方塊物件所公開介面的圖表](images/com06.png)

您可以從圖表中看到， [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 的直接上階是 [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) 介面，接著會繼承 [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow)。 當您將繼承鏈從 **IFileOpenDialog** 移至 **IModalWindow** 時，介面會定義逐漸一般化的視窗功能。 最後， **IModalWindow** 介面會繼承 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)。 一般專案對話方塊物件也會執行存在於不同繼承鏈中的 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)。

現在假設您有一個指向 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 介面的指標。 您要如何取得 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 介面的指標？

![顯示兩個介面指標指向相同物件之介面的圖表](images/com07.png)

只要將 [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 指標轉換成 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 指標就無法運作。 沒有可靠的方法可跨繼承階層進行「交叉轉型」，而不會有某種形式的執行時間類型資訊 (RTTI) ，也就是與語言相依的高度特性。

COM 方法是 *要求* 物件提供您 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 的指標，並使用第一個介面做為物件的管道。 這是藉由從第一個介面指標呼叫 [**IUnknown：： QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法來完成。 在 c + + 中，您可以將 **QueryInterface** 視為 **動態 \_ 轉換** 關鍵字的語言獨立版本。

[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法具有下列簽章：

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

根據您對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的熟悉程度，您或許可以猜測 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 的運作方式。

-   *Riid* 參數是識別您所要求之介面的 GUID。 資料類型 **REFIID** 是的 **typedef** `const GUID&` 。 請注意，因為物件已經建立，所以不需要 (CLSID) 的類別識別碼。 只有介面識別碼是必要的。
-   *PpvObject* 參數會接收介面的指標。 此參數的資料類型為 **\* \* void**，原因是 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)會使用此資料類型： [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))可用來查詢任何 COM 介面，因此參數不能是強型別。

以下是呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) 指標的方法：


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



如往常一樣，請檢查 **HRESULT** 傳回值（如果方法失敗）。 如果方法成功，您就必須在使用指標完成時呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) ，如 [管理物件的存留期](managing-the-lifetime-of-an-object.md)所述。

## <a name="next"></a>下一個

[COM 中的記憶體配置](memory-allocation-in-com.md)

 

 