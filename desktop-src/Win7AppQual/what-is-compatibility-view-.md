---
description: 什麼是相容性檢視？
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: 什麼是相容性檢視？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be51f94d560d206c579d74d9407d53541205201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113396"
---
# <a name="what-is-compatibility-view"></a>什麼是相容性檢視？

*相容性檢視* 是 windows Internet Explorer 8 的一項功能，可讓瀏覽器轉譯網頁的方式幾乎與 Windows Internet Explorer 7 轉譯網頁的方式相同。

在 Internet Explorer 8 中，相容性檢視變更瀏覽器如何解讀以 CSS、HTML 和檔物件模型 (DOM) 撰寫的程式碼，以嘗試符合 Internet Explorer 7。 使用者在 Internet Explorer 8 相容性檢視中所觀看的網站，與使用者在 Internet Explorer 7 中所流覽的網站幾乎完全相同。 不過，相容性檢視不會變更瀏覽器解讀所有程式碼的方式。 例如，在 Internet Explorer 8 中，瀏覽器如何處理 ActiveX、剖析器、AJAX、JavaScript、網路和安全性的變更可能仍會造成相容性問題。 相容性檢視不會變更這些行為。

在企業環境中，某些區域對於相容性問題的風險較低。 例如，內部網路區域網站預設會使用相容性檢視。 使用網頁瀏覽器控制項轉譯的用戶端 web 應用程式，或 WebOC (Internet Explorer 轉譯引擎) ，對於相容性問題也有很低的風險，因為 Internet Explorer 8 預設為 WebOC 的相容性模式。 不過，相容性檢視的預設設定可能無法確保完全相容。 若要判斷網站或 web 應用程式是否與 Internet Explorer 8 相容，您應該測試網站或 web 應用程式。

如需 Internet Explorer 8 相容性檢視與 Internet Explorer 7 之間差異的詳細資訊，請參閱 [網站相容性和 Internet Explorer 8 的 blog](/archive/blogs/ie/site-compatibility-and-ie8)。 如需升級至 Internet Explorer 8 時要檢查的事項清單，請參閱 [Internet Explorer 8 準備工具](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx)組。

如需相容性檢視的詳細資訊，請參閱 [Internet Explorer Team Blog](/archive/blogs/ie/)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
