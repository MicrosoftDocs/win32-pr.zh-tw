---
title: " (的 VML) 附錄"
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- 網路研討會，命名空間
- 網路研討會，行為樣式
- 設計網頁、命名空間
- 設計網頁、行為樣式
- Vector Markup Language (VML) 、命名空間
- VML (Vector Markup Language) 、命名空間
- 向量圖形，命名空間
- Vector Markup Language (VML) 、行為樣式
- VML (Vector Markup Language) 、行為樣式
- 向量圖形，行為樣式
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640de79138adcc345d4352ead814195007b88e0714a0f89816819d545e6e1ef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512608"
---
# <a name="appendix-vml"></a> (的 VML) 附錄

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

若要讓瀏覽器知道如何將資料交給 VML 特定的處理器，您需要輸入一些資訊，例如命名空間和行為樣式。 然後，您可以使用 VML 來輸入區域中的圖形 `<BODY>` 。

本主題內容：

-   [命名空間](#namespaces)
-   [行為樣式](#behavior-styles)

## <a name="namespaces"></a>命名空間

XML 機制指出元素的命名空間。 如果您從 HTML 中的剖析切換到 XML 中的剖析，此機制會指出 HTML 內的參數。

要求 vender 您的 VML 處理器需要 XML 命名空間所需的資訊。

如果您使用 Microsoft Internet Explorer 轉譯 VML，請一律在標記中輸入下列程式 `<HTML>` 程式碼：


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



當剖析具有前置詞的 XML 標記 `v:` ，並將產生的資料交給 vml 處理器時，此資訊會告訴 Internet Explorer 切換至命名空間 "urn：架構-microsoft-com： vml"。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="behavior-styles"></a>行為樣式

在 Microsoft Internet Explorer 中，會將 VML 定義為預設行為。

若要轉譯 VML，請一律在區域中輸入下列幾行 `<HEAD>` ：


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



在 Internet Explorer 中，會透過 VGX.DLL 來執行 VML。 如果您的瀏覽器初始安裝未包含 VML 行為，您可能需要將它新增為選項。 您不需要新增 `<object>` 標記。

 

 
