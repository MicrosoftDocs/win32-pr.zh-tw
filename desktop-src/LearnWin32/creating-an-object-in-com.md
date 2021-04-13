---
title: 在 COM 中建立物件
description: 若要使用 COM 介面，您的程式首先會建立物件的實例，該實例會執行該介面。
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375136"
---
# <a name="creating-an-object-in-com"></a>在 COM 中建立物件

執行緒初始化 COM 程式庫之後，就可以安全地讓執行緒使用 COM 介面。 若要使用 COM 介面，您的程式首先會建立物件的實例，該實例會執行該介面。

一般情況下，有兩種方式可以建立 COM 物件：

-   執行物件的模組可能會提供特別設計的函式，以建立該物件的實例。
-   此外，COM 也提供名為 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的一般建立函數。

例如，從主題的「 `Shape` [什麼是 COM 介面](what-is-a-com-interface-.md)」取得假設的物件。 在該範例中， `Shape` 物件會執行名為的介面 `IDrawable` 。 執行物件的圖形程式庫 `Shape` 可能會使用下列簽章匯出函式。


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



指定此函式時，您可以建立新的物件，如下所示 `Shape` 。


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



*PpShape* 參數的類型為指標 to `IDrawable` 。 如果您之前未看到此模式，可能會令人困惑雙重間接取值。

請考慮函數的需求 `CreateShape` 。 函數必須將 `IDrawable` 指標傳回給呼叫端。 但函數的傳回值已用於錯誤/成功碼。 因此，指標必須透過函數的引數傳回。 呼叫端會將類型的變數傳遞 `IDrawable*` 至函式，而函式會以新指標覆寫此變數 `IDrawable` 。 在 c + + 中，有兩種方式可讓函式覆寫參數值：以傳址方式傳遞，或依位址傳遞。 COM 使用後者的傳遞位址。 指標的位址是指標指標，所以參數型別必須是 `IDrawable**` 。

以下的圖表可協助您以視覺化方式呈現進展。

![顯示雙指標間接取值的圖表](images/com03.png)

`CreateShape`函數會使用 *pShape* (的位址 `&pShape`) 將新的指標值寫入 *pShape*。

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance：建立物件的一般方式

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函數提供用來建立物件的一般機制。 若要瞭解 **CoCreateInstance**，請記住，有兩個 COM 物件可以執行相同的介面，而一個物件可執行兩個或多個介面。 因此，建立物件的泛型函數需要兩項資訊。

-   要建立的物件。
-   要從物件取得的介面。

但是，我們要如何在呼叫函式時指出這種資訊呢？ 在 COM 中，物件或介面是藉由指派128位數位（稱為 *全域唯一識別碼* (GUID) 來識別）。 Guid 會以讓它們有效的方式產生。 Guid 是一種解決方法，可解決如何建立沒有中央登錄授權單位的唯一識別碼。 Guid 有時也稱為 *通用唯一識別碼* ， (uuid) 。 在 COM 之前，它們用於 DCE/RPC (分散式運算環境/遠端程序呼叫) 。 有數種演算法可用於建立新的 Guid。 並非所有這些演算法都能完全保證唯一性，但是不小心建立相同 GUID 值的機率相當小，實際上是零。 Guid 可以用來識別任何類型的實體，而不只是物件和介面。 不過，這是我們在此課程模組中唯一關心的用途。

例如，連結 `Shapes` 庫可能會宣告兩個 GUID 常數：


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



 (您可以假設這些常數的實際128位數值是在其他地方定義的。 ) 常數 **CLSID \_ 圖形** 可識別 `Shape` 物件，而常數 **IID \_ IDrawable** 則可識別 `IDrawable` 介面。 前置詞 "CLSID" 代表 *類別識別碼*，而前置詞 *IID* 代表 *介面識別碼*。 這些是 COM 中的標準命名慣例。

指定這些值之後，您會建立新的實例，如下所示 `Shape` ：


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)函數有五個參數。 第一個和第四個參數是類別識別碼和介面識別碼。 實際上，這些參數會告訴函式「建立繪圖物件，並提供 IDrawable 介面的指標」。

將第二個參數設定為 **Null**。  (如需此參數意義的詳細資訊，請參閱 COM 檔集中的主題 [匯總](/windows/desktop/com/aggregation) 。第三個參數 ) 第三個參數會採用一組旗標，其主要目的是要指定物件的 *執行內容* 。 執行內容會指定物件是否在與應用程式相同的進程中執行;在同一部電腦的不同處理常式中;或在遠端電腦上。 下表顯示此參數最常用的值。



| 旗標                       | 描述                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSCTX \_ INPROC \_ 伺服器** | 相同的進程。                                                                                                                                                      |
| **CLSCTX \_ 本地 \_ 伺服器**  | 不同的處理常式，相同的電腦。                                                                                                                                  |
| **CLSCTX \_ 遠端 \_ 伺服器** | 不同的電腦。                                                                                                                                                |
| **CLSCTX \_ 全部**            | 使用物件支援的最有效率選項。 從最有效率到最有效率的等級 (排名是：同進程、跨進程，以及跨電腦。 )  |



 

特定元件的檔可能會告訴您該物件所支援的執行內容。 如果不是，請使用 [ **\_ 全部 CLSCTX**]。 如果您要求物件不支援的執行內容， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數會傳回錯誤碼 **REGDB \_ E \_ CLASSNOTREG**。 這個錯誤碼也可以指出 CLSID 沒有對應到使用者電腦上註冊的任何元件。

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的第五個參數會接收介面指標。 因為 **CoCreateInstance** 是泛型機制，所以這個參數不能是強型別。 相反地，資料類型為 **void \* \***，而且呼叫端必須將指標的位址強制轉型為 **void \* \*** 型別。 這是在上一個範例中 **重新解譯 \_ 轉換** 的目的。

檢查 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)的傳回值是很重要的。 如果函式傳回錯誤碼，則 COM 介面指標無效，而嘗試對其進行取值可能會導致您的程式損毀。

就內部而言， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數會使用各種技術來建立物件。 在最簡單的情況下，它會查閱登錄中的類別識別碼。 登錄專案會指向用來執行物件的 DLL 或 EXE。 **CoCreateInstance** 也可以使用 com + 類別目錄中的資訊，或並存的 (SxS) 資訊清單。 無論何者，詳細資料對呼叫端都是透明的。 如需有關 **CoCreateInstance** 內部詳細資料的詳細資訊，請參閱 [COM 用戶端和伺服器](/windows/desktop/com/com-clients-and-servers)。

`Shapes`我們使用的範例有點假設，所以現在讓我們來看看一個實際的 COM 範例：顯示 [**開啟**] 對話方塊，讓使用者選取檔案。

## <a name="next"></a>下一個

[範例：開啟對話方塊](example--the-open-dialog-box.md)

 

 