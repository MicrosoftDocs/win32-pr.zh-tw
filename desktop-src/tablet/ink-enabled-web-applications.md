---
description: 筆墨 Blog 範例會示範幾個實用的技巧，可用於啟用筆墨的 Web 應用程式。
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Ink-Enabled Web 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8097bd55c34abbcb4469d74642e9dbc9a5f29e3b0b7110a76543fd40f5b1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043489"
---
# <a name="ink-enabled-web-applications"></a>Ink-Enabled Web 應用程式

[筆墨 Blog](ink-blog-web-sample.md)範例會示範幾個實用的技巧，可用於啟用筆墨的 Web 應用程式。 這些包括：測試用戶端電腦是否可以支援啟用筆墨的控制項、將筆墨資料提交至伺服器，以及在網頁上顯示筆墨資料。

## <a name="testing-ink-enablement"></a>測試筆墨啟用

測試用戶端電腦是否可以顯示啟用筆墨的控制項可能很有用。 這可讓您在用戶端為 Tablet PC 或不同的電腦時，thewebpageshow 一個控制項。 測試這項作業的其中一種方式是嘗試[建立一個物件，例如](/previous-versions/ms833057(v=msdn.10))，您只能在已安裝 Windows Vista、Windows xp tablet pc edition 作業系統或 Windows xp tablet pc edition 軟體發展工具組 () SDK 的電腦上建立該物件。 如果您在 try/catch 區塊中建立物件，並攔截任何擲回的例外狀況 (通常會擲回 [FileNotFoundException](/previous-versions/windows/) ，表示找不到具有此控制項的元件) ，您可以偵測用戶端電腦是否可以支援啟用筆墨的控制項。 在此範例中，您可以在類別的函式中找到此程式碼 `InkArea` 。

## <a name="submitting-ink-data"></a>提交筆墨資料

提交資料的簡單方法是從啟用筆墨的控制項取出資料，將它傳送至隱藏的表單，然後提交表單。 您可以使用 [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) 方法將筆墨序列化，然後轉換成字串。 在範例中，隱藏的表單是在 AddBlog 中定義，而筆墨序列化則是在中處理 `InkArea.SerializeInkData` ，其中筆墨會序列化為 GIF 影像。  (請注意，它也可以用類似于其他格式的方式序列化，例如筆墨序列化格式 (ISF) 。 ) 

## <a name="displaying-ink-data"></a>顯示筆墨資料

在範例中，AddBlog 會有一個方法，這個方法會抓取 `Page_Load` 張貼至伺服器的資料，並將它儲存到檔案中。 然後，它會在伺服器上產生網頁，其中包含以 GIF 影像參考檔案的 img 標記。 現在您只需要流覽至這些頁面，即可看到筆墨的影像。  (請注意，如果您已使用不同的格式（例如筆跡序列化格式 (ISF) ）將筆墨序列化，就必須將筆墨轉換成伺服器上的影像，才能將它顯示在非平板電腦的用戶端上。 ) 

Tablet PC 用戶端可以將筆墨載入啟用筆墨的控制項，並允許使用者使用 ISF 來編輯筆墨。 即使是使用 [PersistenceFormat](/previous-versions/ms827245(v=msdn.10))列舉的 **Gif** 值所儲存的筆墨也是如此，因為 ISF 資料是包含在 gif 中繼資料中。

 

 
