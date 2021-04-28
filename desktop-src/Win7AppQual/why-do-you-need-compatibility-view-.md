---
description: 為什麼需要相容性檢視？
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: 為什麼需要相容性檢視？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9991e9dc0c2edcd66ae6655c094f17b240be985a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113376"
---
# <a name="why-do-you-need-compatibility-view"></a>為什麼需要相容性檢視？

相容性檢視功能會遵循一組規則，以正確顯示內容，而不需要任何使用者 (或 IT 系統管理員) 動作（如果可能的話）。 相容性檢視可讓開發人員指示瀏覽器要使用的轉譯引擎，並讓使用者覆寫瀏覽器的選擇和切換模式。 如果開發人員和 IT 專業人員未指定要使用哪種轉譯模式，則使用者會在網址列的右邊看到「中斷的頁面」圖示，如下圖所示。

![網址列旁的中斷頁面圖示圖例](images/iecompatview.png)

如果使用者按一下此圖示，Windows Internet Explorer 8 會切換轉譯模式，並立即重載頁面。

使用者不一定會看到這個圖示。 它是次要解決方案，而不是主要的應用程式相容性機制。 只有當相容性檢視的變更有意義時（例如當使用者流覽標準模式頁面時），Windows Internet Explorer 才會顯示此圖示。 在所有其他情況下，例如當使用者查看 [其他] 模式頁面或 [view 近端內部網路] 區域網站時，不會出現此圖示。 如需相容性檢視的詳細資訊，以及出現圖示時，請參閱 [相容性檢視簡介](/archive/blogs/ie/)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
