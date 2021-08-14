---
description: 分割物件會使用 RecognizerCoNtext 來改善其辨識區段的分析，並產生手寫元素的辨識文字。
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: 使用辨識器內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d99020e97170f0b68b1459abdc4b85f81ebc3fbba426233c2c13b5e042f28ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715096"
---
# <a name="working-with-a-recognizer-context"></a>使用辨識器內容

[**分割**](inkdivider-class.md)物件會使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md)來改善其辨識區段的分析，並產生手寫元素的辨識文字。

您可以使用 [**分隔**](inkdivider-class.md)物件的 [**RecognizerCoNtext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)屬性，或在 managed 程式碼) 的 ([分割](/previous-versions/ms839465(v=msdn.10))函式的呼叫中提供辨識器內容，來設定辨識器內容。 如果非手寫辨識器的辨識器內容，或不支援「免費輸入」功能的辨識器內容指派給 **RecognizerCoNtext** 屬性，則會擲回例外狀況。

如果未安裝辨識器，或未將辨識器內容指派給 [**分割**](inkdivider-class.md) 物件，則 **分隔** 物件不會使用辨識器內容。 在此情況下，版面配置分析功能會執行區段分割，而且沒有任何文字與 [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件相關聯。

> [!Note]  
> 將筆劃指派給 [**分隔**](inkdivider-class.md)物件之後，就無法變更 [**RecognizerCoNtext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)屬性。 **分隔** 物件會使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的預設屬性值。

 

[**分割**](inkdivider-class.md)物件會在版面配置分析期間，將辨識器內容套用至手寫元素。 **分割** 物件會忽略您直接指派給辨識器內容的任何筆觸。 如需文字辨識的詳細資訊，請參閱 [關於手寫辨識](about-handwriting-recognition.md)。

 

 
