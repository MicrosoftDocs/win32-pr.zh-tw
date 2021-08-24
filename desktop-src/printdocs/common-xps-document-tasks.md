---
description: 此頁面會列出一些通常是使用 XPS 檔 API 來執行的程式設計工作。
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: 一般 XPS 檔程式設計工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7f71614344968bcc68e658021e1f34296a595d9fbf58be2d544c03c3dc428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846348"
---
# <a name="common-xps-document-programming-tasks"></a>一般 XPS 檔程式設計工作

此頁面會列出一些通常是使用 XPS 檔 API 來執行的程式設計工作。

## <a name="common-xps-document-tasks"></a>一般 XPS 檔工作

下列程式碼範例說明在使用 xps 檔 API 來處理 XPS OM 時，通常會執行的一些程式設計工作。

<dl>

[初始化 XPS OM](xps-object-model-initialization.md)  
[建立空白的 XPS OM](create-a-blank-xps-om.md)  
[將 XPS 檔讀入 XPS OM](read-an-xps-document-into-an-xps-om.md)  
[流覽 XPS OM](navigate-the-xps-om.md)  
[將文字寫入至 XPS OM](write-text-to-an-xps-om.md)  
[在 XPS OM 中繪製圖形](draw-graphics-in-an-xps-om.md)  
[以 XPS OM 放置影像](place-images-in-an-xps-om.md)  
[將 XPS OM 寫入 XPS 檔](write-an-xps-om-to-an-xps-document.md)  
[列印 XPS OM](print-an-xps-om.md)  
[使用 XPS OM 集合介面](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>免責聲明

程式碼範例的目的不是完整且正常運作的程式。 例如，此頁面所參考的程式碼範例不會執行參數檢查、錯誤檢查或錯誤處理。 使用這些範例作為起點，然後新增建立健全的應用程式所需的程式碼。 如需 **HRESULT** 傳回值和錯誤處理策略的詳細資訊，請參閱 [COM 中的錯誤處理](../com/error-handling-in-com.md)。

在可以使用 XPS OM 介面之前，必須線上程中初始化 COM，如下列範例程式碼所示。


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



為了清楚起見，這些程式碼範例會使用非常簡單的 XPS OM，它對您的應用程式而言可能不夠複雜。 在此情況下，將內容新增至頁面的程式碼範例中，會將頁面的視覺元素直接新增至頁面的視覺物件清單;不過，在實務上，您可能會想要將視覺物件分組為 canvas 物件，以便將多個物件視為群組來處理。 因此，若要啟用多個頁面大小的相同內容支援，您可以將頁面的視覺內容分組成單一畫布物件，然後將轉換套用至畫布，以將其調整為目前的頁面大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的錯誤處理](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
