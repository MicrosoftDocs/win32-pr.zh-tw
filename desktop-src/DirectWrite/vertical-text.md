---
title: 垂直文字
description: 從 Windows 8 開始，DirectWrite 有一些新的 Api，可讓您在應用程式中使用垂直文字。
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db8788a6be97a55911694942a930e17dc69976a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933283"
---
# <a name="vertical-text"></a>垂直文字

從 Windows 8 開始， [DirectWrite](direct-write-portal.md) 有一些新的 api，可讓您在應用程式中使用垂直文字。

## <a name="drawing-vertical-text"></a>繪製垂直文字

您可以使用 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法，以 Direct2D 繪製垂直文字。 若要垂直繪製文字，請將 [**DWRITE 的 \_ 讀取方向從上往 \_ \_ \_ \_ 下**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) 傳遞至 [**IDWriteTextFormat：： SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) 方法，並將 [**DWRITE \_ 流程方向由 \_ \_ 右 \_ \_ 移**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) 至 [**IDWriteTextFormatSetFlowDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) 方法。 然後，您可以建立和繪製垂直 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。

## <a name="analyzing-character-orientation"></a>分析字元方向

每個字元都有一個慣用的字元方向，或字元應該以任何方向配置來導向的方向。 例如，在傳統水準配置中，拉丁文字和中文文字都是垂直方向。 另一方面，在垂直版面配置中，中文文字會保持直立，而拉丁文字會旋轉90度。 此處的範例會顯示這項差異。

![水準和垂直版面配置中的英文和中文文字影像。](images/vertical-text.png)

若要判斷您擁有的文字方向，您需要執行 [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) 和 [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) 介面。 來源和接收會接受圖像執行，並可讓您檢查它們是否為垂直方向。

在您執行來源和接收器之後，請呼叫 [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) 方法。 在範例影像中，此函式會傳回3個回合：「英文」、「中國」和「英文」。

## <a name="going-from-characters-to-glyphs"></a>從字元到字元

現在您已經知道執行包含垂直圖像，您需要取得這些字元的存取權。 在目前為止的範例中，有3個執行：一個具有垂直圖像，另一個則沒有。 若要從字元轉換成字元，您可以呼叫 [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices)。 這個方法會針對範例中的字元傳回對應的圖像索引。 因為 [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) 方法會傳回具有垂直字元的回合，所以您必須呼叫 [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants)，這會傳回垂直方向的圖像 id 以取代目前的圖像 id。

## <a name="drawing-text-vertically"></a>垂直繪製文字

最後，您需要配置和繪製文字。 因為您是以垂直方式繪製文字，所以您需要取得一些資訊，才能正確地繪製拉丁文字。 如果您在中央基準中繪製所有文字，則會在該行中間以浮點數顯示拉丁文字。 您需要存取中央和羅馬字基準才能正確對齊文字。 使用 [**IDWriteTextAnalyzer1：： GetBaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) 方法，取得您指定之基準的數值。 您可以從中央基準減去羅馬字基準，以取得兩者之間的位移。

使用這些資訊，您可以在螢幕上繪製文字。 首先，使用 [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1)和 [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1)物件的結果來呼叫 [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform)方法。

如果您使用的是 [Direct2D](rendering-by-using-direct2d.md) ，也必須在 Direct2D 轉譯目標上設定「世界」轉換，以進行垂直轉譯。

最後，呼叫 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 三次，在每個文字區塊上呼叫一次。 在兩個英文的文字區塊上，您必須套用在羅馬和 central 基準之間計算的位移。

現在，您應用程式中的文字會以正確的字元方向垂直繪製。

 

 