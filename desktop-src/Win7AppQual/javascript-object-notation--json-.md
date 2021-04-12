---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JavaScript 物件標記法 (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193270"
---
# <a name="javascript-object-notation-json"></a>JavaScript 物件標記法 (JSON)

[JavaScript 物件標記法 (JSON) ](https://www.json.org/) 是簡單且輕量的資料交換格式，此格式是以 JavaScript 語言的物件常值標記法子集為基礎。 Windows Internet Explorer 8 中的 JavaScript 引擎會為原生 JSON (處理函式（使用[Douglas Crockford 的 json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)) ）實行[ECMAScript 3.1 JSON 提案](https://www.ecma-international.org/)。

Internet Explorer 8 包含原生 JSON 物件，此物件符合「 [es 3.1 提案工作草稿](https://www.ecma-international.org/)」中所述的 JSON 支援。 某些網頁會偵測到原生 JSON 物件，然後以非標準方式使用它。 此使用通常會導致腳本錯誤，並中斷 AJAX 要求的處理。 下列程式碼範例顯示使用 JSON 物件的錯誤方式。


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



相反地，下列程式碼範例會顯示使用 JSON 物件的好方法。


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer 包含原生的 JSON 支援，方法是引進具有兩個內建方法的全域 JSON 物件： **json.stringify** 和 **parse**。 全域 JSON 物件是在 JavaScript 引擎中定義，並且會在引擎初始化階段期間建立。 為了維持回溯相容性，只有當網站使用最新版的 JavaScript 功能時，才能使用「Internet Explorer 8 標準」配置 (檔) 模式。 這項功能也可能會影響依賴全域變數 JSON 或使用 [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)之網頁的行為。

您可以覆寫全域 JSON 物件。 但是，當網頁使用「Internet Explorer 8 標準」配置 (檔) 模式時，它再也不是未定義的物件。 因為 JavaScript 引擎會將 JSON 具現化為全域名稱，所以會檢查「如果 (！ this.JSON) 」是否評估為 False，而且必須在使用者程式碼中變更。

使用 [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) 的網頁可能不會受到影響。 有幾個例外狀況，這些頁面應該可以更快速地運作。 例外狀況是因為 Internet Explorer 原生 JSON 執行和 json2.js 之間的差異。 例如，在序列化期間，原生 JSON 實作為偵測迴圈，而不會進入無限遞迴（例如 json.js）。 如需這些例外狀況的詳細資訊，請參閱 [JavaScript blog](/archive/blogs/jscript/)。

如需詳細資訊，請參閱 [JSON 檔](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) 和 [版本控制和 JavaScript 引擎的版本支援](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
