---
description: 標準注釋和語義 (DXSAS) 提供以標準方式使用著色器的方法，可讓著色器用於工具、應用程式和遊戲引擎。
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: DirectX 標準注釋和語義參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c989f4aed7c01c62d6133e01fe035223b74c8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467685"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>DirectX 標準注釋和語義參考

標準注釋和語義 (DXSAS) 提供以標準方式使用著色器的方法，可讓著色器用於工具、應用程式和遊戲引擎。 DXSAS 會針對共用效果，定義一組附加至主應用程式值和效果參數的一組語義和批註。 為了讓這些批註和語義都能發揮效用，必須同時在主應用程式和效果檔案中執行它們。 本檔說明利用 DirectX 效果架構強大功能的 DXSAS 標準，可讓主應用程式和工具以程式設計的方式)  ( fx 檔案共用 DirectX 效果，以及設計與 UI 的互動。

## <a name="background-information"></a>背景資訊

標準注釋和語義是設計用來系結效果和 X 檔案參數，以裝載應用程式值。 D3DX 效果架構 (或效果) 封裝呈現狀態。 藉由封裝轉譯狀態 (（包括頂點、材質和圖元處理狀態）) 效果中，您可以建立效果的程式庫，其中涵蓋各式各樣的呈現選項。 這可能包括在不同硬體類型上轉譯的選項，或使用單一或多重行程混合進行轉譯的選項。 如需效果架構的詳細資訊，請參閱 [效果參考](dx9-graphics-reference-effects.md)。 DXSAS 建置於這個架構之上，讓開發人員能獲得更一致的體驗。 當轉譯設定封裝成效果之後，DXSAS 標準可讓效果開發人員透過注釋公開效果參數的意圖。 然後，任何主機應用程式或工具都可以讀取這些注釋 (而不只是設計用來使用符合標準之效果) 的注釋，也可以瞭解如何以設計方式使用效果。

將裝載應用程式所支援的效果語義和注釋標準化，可讓效果作者建立可在多個專案中使用的效果，進而提升更廣大的效果使用者組合。 DXSAS standard 讓開發人員可以讀取檔案，在工具之間交換，並讓開發人員利用協力廠商工具來撰寫管線的效果。

本檔說明使用注釋表達效果參數意圖的 DXSAS 標準，以及定義主應用程式同意可讓其生效的主應用程式值集合。

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>使用標準注釋和語義撰寫效果

如下圖所示，DXSAS 標準需要效果檔案中的批註，以及遵循此處所述指導方針的主應用程式來處理檔案。

![主機應用程式和效果檔案的 dxsas 標準圖表](images/sas-2.png)

主應用程式必須執行使用者介面邏輯和主機環境。 若要執行 DXSAS 相容效果，請閱讀下列主題：

-   [全域參數](global-parameter.md)會定義效果的相關資訊，例如版本或效果作者。
-   [資料](data-binding.md) 系結會定義參數的集合 (以及其型別和結構) ，可由可由主應用程式所設定的效果所使用的效果來設定。
-   若要將使用者介面控制項與效果參數產生關聯，請使用 [UI 注釋](ui-annotation.md)。 這些批註包括： [SasUiMax](ui-annotation.md)、 [SasUiMin](ui-annotation.md)、 [SasUiSteps](ui-annotation.md)、 [SasUiStepsPower](ui-annotation.md)和 [SasUiStride](ui-annotation.md)。
-   若要使用外部檔案中包含的資料來初始化效果參數，請使用 [參數初始化注釋](parameter-initialization-annotation.md)。
-   當主應用程式和效果之間的資料傳輸 (或反之亦然) ，當類型不完全相符時，就會發生 [轉換和轉換](casting-and-conversion.md) 。 此區段指定當來源和目標型別不同時，如何寫入資料。 此外，您也可以使用 [ParameterValueModifiers](casting-and-conversion.md) 來修改主機應用程式應該如何解讀從效果參數讀取的資料。 這些批註包括： [SasNormalize](casting-and-conversion.md) 和 [SasUnits](casting-and-conversion.md)。

## <a name="case-sensitivity"></a>區分大小寫

所有識別碼、語義和批註值都不區分大小寫。 批註名稱 (不) 值會區分大小寫。 批註名稱可由 D3DX 效果系統辨識，因此 SAS 批註名稱也是如此。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果參考](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



