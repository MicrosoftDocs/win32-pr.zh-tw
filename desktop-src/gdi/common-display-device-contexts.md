---
description: 一般裝置內容會用於在視窗的工作區中繪製。
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: 一般顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d9de2d9908be735d959a85ca6bdfe99abf7f33489c74175ab2882551393cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105687"
---
# <a name="common-display-device-contexts"></a>一般顯示裝置內容

*一般裝置內容* 會用於在視窗的工作區中繪製。 系統預設會針對視窗類別未明確指定顯示裝置內容樣式的視窗，提供通用的裝置內容。 一般的裝置內容通常會與 windows 搭配使用，而不會對裝置內容屬性進行廣泛的變更。 常見的裝置內容很方便，因為它們不需要額外的記憶體或系統資源，但如果應用程式必須在使用之前先設定許多屬性，就很不方便。

系統會從顯示裝置內容快取抓取所有常見的裝置內容。 應用程式可以在建立視窗後立即取得一般裝置內容。 由於一般裝置內容是來自快取，因此應用程式必須在繪製之後儘快釋放裝置內容。 一般裝置內容釋出之後，將不再有效，而且應用程式不能嘗試使用它來繪製。 若要再次繪製，應用程式必須抓取新的一般裝置內容，並在每次在視窗中繪製時，繼續取出並釋放一般裝置內容。 如果應用程式使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式來抓取裝置內容控制碼，它必須使用 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放控制碼。 同樣地，對於每個 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函數，應用程式都必須使用對應的 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函式。

當應用程式抓取裝置內容時，系統會調整原點，使其符合工作區的左上角。 它也會設定裁剪區域，以便將裝置內容的輸出裁剪到工作區。 否則會裁剪任何在用戶端區域以外出現的輸出。 如果應用程式使用 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)來抓取一般裝置內容，則系統也會在裁剪區域中包含更新區域，以進一步限制輸出。

當應用程式釋放一般裝置內容時，系統會還原裝置內容之屬性的預設值。 修改屬性值的應用程式必須在每次抓取通用裝置內容時這麼做。 釋出裝置內容會釋出應用程式可能已選取的繪圖物件，因此應用程式不需要在釋出裝置內容之前釋放這些物件。 在所有情況下，應用程式絕對不能假設一般裝置內容會在發行後保留非預設的選取專案。

 

 



