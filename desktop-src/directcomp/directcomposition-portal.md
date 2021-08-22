---
title: DirectComposition
description: 本主題說明 Microsoft DirectComposition 的用途、識別其執行時間需求，並說明有效使用 Microsoft DirectComposition 所需的程式設計背景。
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- DirectComposition API
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1b13dbd0ee4893f1b208cd88d7fd1251b5fb7ece2400b7e0b195e84865b2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985408"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 Windows 的撰寫 api，而不是 DirectComposition。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

## <a name="purpose"></a>目的

Microsoft DirectComposition 是一個 Windows 元件，可透過轉換、效果和動畫來提供高效能點陣圖組合。 應用程式開發人員可以使用 DirectComposition API 來建立視覺上吸引人的使用者介面，以提供豐富和流暢的動畫轉換 (從一種視覺效果轉換成另一種視覺效果)。

DirectComposition 可讓您藉由使用圖形硬體，以及獨立于 UI 執行緒之外運作的方式，來達到豐富且流暢的轉換。 DirectComposition 可以接受由不同轉譯程式庫（包括 Microsoft DirectX 點陣圖）所繪製的點陣圖內容，以及轉譯成視窗 (HWND 點陣圖) 的點陣圖。 此外，DirectComposition 還支援各種不同的轉換，例如2D 仿射轉換和3D 透視圖的轉換，以及像是裁剪和不透明度的基本效果。

DirectComposition 的設計目的是要簡化撰寫 [*視覺效果*](directcomposition-glossary.md) 和建立動畫轉換的流程。 如果您的應用程式已經包含轉譯程式碼，或已經使用建議的 DirectX API，您只需要執行最少量的工作，就能有效地使用 DirectComposition。

## <a name="developer-audience"></a>開發人員對象

DirectComposition API 適用于熟悉 C/c + + 的經驗豐富且具備高度能力的圖形開發人員，對於元件物件模型 (的 COM) 有充分的瞭解，並熟悉 Windows 程式設計概念。

## <a name="run-time-requirements"></a>執行階段需求求

DirectComposition 是在 Windows 8 引進。 它包含在32位、64位和 ARM 平臺中。

## <a name="in-this-section"></a>本節內容



| 主題                                                                       | 描述                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [為何要使用 DirectComposition？](why-use-directcomposition-.md)<br/>     | 本主題說明 DirectComposition 的功能和優點。 <br/>                                                                           |
| [如何使用 DirectComposition](how-to-use-directcomposition.md)<br/> | 本節說明使用 DirectComposition API 的最佳作法，並示範如何使用 API 來完成數個常見的工作。 <br/> |
| [DirectComposition 概念](directcomposition-concepts.md)<br/>     | 本節提供 DirectComposition 的概念總覽。<br/>                                                                                   |
| [DirectComposition 參考](reference.md)<br/>                     | 本節提供組成 DirectComposition API 之元素的詳細參考資訊。<br/>                                       |
| [DirectComposition 範例](directcomposition-code-samples.md)<br/>  | 下列範例應用程式會示範如何使用 DirectComposition API，並示範其功能。 <br/>                                      |
| [DirectComposition 詞彙](directcomposition-glossary.md)<br/>     | 本主題定義 DirectComposition 條款。 <br/>                                                                                                        |



 

 

 





