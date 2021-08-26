---
description: 您通常會想要複製一組更複雜的資訊，而不是可 (ISF) 的筆墨序列化格式。
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: 以 HTML 儲存筆墨
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8949582c5743ba7be5ac664627792c7b7f8a0cd5968a67f5db08b6428cb886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934358"
---
# <a name="storing-ink-in-html"></a>以 HTML 儲存筆墨

您通常會想要複製一組更複雜的資訊，而不是可 (ISF) 的筆墨序列化格式。 HTML 特別適用于互通性格式，因為它會以業界標準的形式接受，以及其代表異類內容的能力。

HTML 已廣泛理解、妥善記載，並熟悉許多開發人員。 有許多適用于 HTML 生產的工具。 此外，Microsoft Windows 包含應用程式開發介面， (api) 以轉譯和操作 HTML。 最後，Tablet PC 平臺 Api 提供嚴加防禦 GIF 持續性格式，適用于以其他格式內嵌，最重要的是 HTML。 此格式是由 GIF 檔案所組成，其中包含內嵌在應用程式延伸模組區塊中筆跡序列化格式 (ISF) 。

這些 GIF 檔是筆墨物件的標記法：

-   在未啟用筆墨的應用程式中轉譯，例如瀏覽器或舊版字處理器。
-   包含原始筆跡中的所有必要資訊，而這些資訊是為了進行編輯或辨識等用途而想要維護的。

這些 GIF 檔案可以使用 Tablet PC 平臺 Api 的持續性方法來產生。 它們是 Gif，而且應該使用 GIF 擴充功能，而如果應用程式不是啟用筆墨，就不會有任何不同的標準 GIF。 不過，對啟用筆墨的應用程式來說，有一組豐富的資料基礎是影像。

在 Tablet PC 平臺 Api 產生之後，HTML 中的 IMG 標記會參考嚴加防禦 GIF。 然後 HTML 會儲存在標準 CF HTML 剪貼簿位置中 \_ 。 這可讓其他應用程式看到 HTML，不論它們是否為啟用筆墨。 映射本身可以儲存在 Windows 的網際網路快取中，並設定為在適當的一段時間後到期。

提供或要求 IMG 標記的特定裝飾。 這些裝飾會將 HTML 識別為包含筆墨。 下列範例會使用 HTML 標籤來參考嚴加防禦 GIF：

`<img href="34372423432.gif" />`

如果需要以其他方式（例如級聯樣式表或 Vector Markup Language (VML) ）參考影像，則應該仍會有參考影像的 IMG 標記。 這可讓您在接受 HTML 表示筆墨的任何應用程式中進行剪下和貼上。

以 HTML 支援筆墨的應用程式應該：

-   \_當使用者執行複製時產生 CF HTML。 在 \_ 複製 (上產生 CF HTML 或另存為 HTML) 時， [](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90))請使用 PersistenceFormat 值，在 *p* 參數中指定 [](/previous-versions/ms827245(v=msdn.10))值，以產生嚴加防禦 GIF 影像。 替代文字應設定為最精確的辨識結果。 您可以視需要將定位設定為絕對或就地。
-   檢查所有的 IMG 標籤，以判斷是否有任何影像指向包含筆墨的影像（如果已選擇要貼上的 CF HTML 位置） \_ 。 如果是的話，請在內部將影像視為 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件。 雖然此版本只支援 GIF 檔案，但在未來支援其他影像格式的情況下，您的應用程式也應該檢查非 GIF 影像。
-   支援對 ISF 的複製和貼上。 支援 HTML 的應用程式也應該支援 ISF，以增強無法辨識 HTML 之啟用筆墨的應用程式的互通性。 這類似于將 HTML 放在剪貼簿上的應用程式也會放置文字的慣例。

如需嚴加防禦 Gif 的詳細資訊，請參閱 [建立區塊](building-blocks.md)。

 

 
