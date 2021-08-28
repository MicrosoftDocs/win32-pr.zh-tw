---
title: Media-Type 協商
description: 許多應用層網際網路通訊協定是以簡單、彈性的格式（稱為多用途網際網路郵件延伸 (MIME) ）作為基礎來交換訊息。
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8d9e2694d7df89eeeef8c0a3e7217a88c3bac27da3e68c38aae2ceae24fa56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130190"
---
# <a name="media-type-negotiation"></a>Media-Type 協商

許多應用層網際網路通訊協定是以簡單、彈性的格式（稱為多用途網際網路郵件延伸 (MIME) ）作為基礎來交換訊息。 雖然 MIME 是以交換電子郵件訊息的標準來產生的，但目前由各種不同的應用程式使用，以指定以 MIME 或媒體類型表示的相互理解資料格式。 此程式稱為 *媒體類型的協商*。

媒體類型是表示類型和子類型 (的簡單字串，例如 "text/純文字" 或 "text/HTML" ) 。 它們可用來標記資料或限定要求。 例如，網頁瀏覽器（例如，HTTP 要求資料或要求資訊的一部分）指定要求「影像/gif」或「影像/jpeg」媒體類型，而網頁伺服器會藉由傳回適當的媒體類型來回應該媒體類型，如果呼叫是要求的資料，則是要求格式的資料本身。

媒體類型的協商通常類似于現有的桌面應用程式如何與系統剪貼簿協調，以決定當使用者在拖放作業期間，于接收 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 指標時選擇編輯/貼上或查詢格式時要貼上的資料格式。 HTTP 媒體型別協商的微妙差異在於，用戶端事先不知道伺服器可以使用的格式。 因此，用戶端會以最精確的精確度來指定支援的媒體類型，而伺服器會以最佳的可用格式來回應。

URL 標記可支援媒體類型的協商，讓網際網路用戶端和伺服器同意在 [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 作業中下載資料時使用的格式。 為了支援媒體類型的協商，用戶端會執行 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) 介面，並呼叫 [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) 函式來向系結內容註冊。 格式列舉值會列出用戶端可以接受的格式。 當系結至 HTTP Url 時，URL 標記會將這些格式轉譯為媒體類型。

用戶端要求的可能媒體類型會透過系結內容上呼叫端所註冊之 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc)列舉值中所提供的 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構，向 URL 名字值表示：每個 **FORMATETC** 都會指定可識別媒體類型的剪貼簿格式。 例如，下列程式碼片段會指定媒體類型為 PostScript。

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

用戶端可以將剪貼簿格式設定為特殊媒體類型 CF \_ Null，以指出應抓取 URL 所指向之資源的預設媒體類型。 這種格式通常是用戶端感興趣的最後一種格式。 如果沒有向系結內容註冊列舉值，URL 的名字會像是包含具有 **cfFormat**= CF Null 之單一 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)的列舉值 \_ 可供使用，並自動下載預設媒體類型。

無論使用哪種類型的媒體類型，用戶端都會透過其 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))方法上的 *pformatetc* 引數來通知選擇。 回呼會發生在用戶端呼叫 [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage)的內容中。

> [!Note]  
> 如果接收的內容是無法辨識的媒體類型，用戶端會自動呼叫 [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) 來註冊新的類型。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[URL 的名字](url-monikers.md)
</dt> </dl>

 

 