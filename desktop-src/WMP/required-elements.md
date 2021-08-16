---
title: 必要元素
description: 必要元素
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player行動外觀、元素
- 外觀，元素
- 外觀定義檔，元素
- 元素、外觀定義檔
- Windows Media Player Mobile 的元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18433e20c914cdc4b276857f97aab6a692d1d11c811660c73620b09a5b9a0f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746307"
---
# <a name="required-elements"></a>必要元素

您必須在您的外觀定義檔中提供下列元素：

-   **頭。** 需要主要的外觀定義檔案標頭。 如需標頭版本資訊，請參閱 [建立面板定義](creating-a-skin-definition-file.md) 檔一節中的表格。
-   **描述區段。** 為 Windows Mobile 的 Windows Media Player 9 系列建立面板時，需要描述區段。 它必須是面板定義檔中的第一個區段，而且必須為維度指定有效的值。 您可以選擇是否要指定方向的值。
-   **點陣圖區段。** 需要點陣圖區段。 此外，點陣圖區段必須指定背景、停用、推送、區域和超級影像檔案的有效名稱。
-   **影像檔。** 您必須提供背景、停用、推送、區域和超級影像檔案作為面板的一部分。 如果您要建立 Windows Media Player 10 行動裝置版或更新版本的面板，則不需要包含區域或超級影像檔案。

如果您建立只定義影像的面板，則會顯示該面板，但不會對使用者提供任何有意義的功能。 如果您決定建立沒有按鈕的面板，或許是為了防止使用者略過某些內容，請注意，您仍然可以將功能對應至裝置上的硬體按鈕。

需要 Thumb 檔案，而且您的 trackbars 不能使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀定義檔**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




