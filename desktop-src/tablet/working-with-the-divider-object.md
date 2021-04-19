---
description: 分隔物件提供對 Tablet PC 版面配置分析功能的存取。
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: 使用分隔物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd158f85d368d764bce17e8b481ebe625a4d6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970981"
---
# <a name="working-with-the-divider-object"></a>使用分隔物件

[分隔](/previous-versions/ms583616(v=vs.100))物件提供對 Tablet PC 版面配置分析功能的存取。

在 managed 程式碼中，您可以呼叫其中一個[分隔](/previous-versions/ms839465(v=msdn.10))器函式來具現化[分割](/previous-versions/ms583616(v=vs.100))物件。 在自動化中，這稱為 [**InkDivider**](inkdivider-class.md) 物件，可透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

您可以藉由呼叫[分隔](/previous-versions/ms583616(v=vs.100))物件的[除法](/previous-versions/ms839461(v=msdn.10))方法，取得目前分析結果的快照。 分析結果會在 [DivisionResult](/previous-versions/ms839371(v=msdn.10)) 物件中傳回。 每次您呼叫除法方法時，分界線物件就會建立 DivisionResult 物件。 如需 DivisionResult 物件的詳細資訊，請參閱 [使用 DivisionResult 物件](working-with-the-divisionresult-object.md)。

[分割](/previous-versions/ms583616(v=vs.100))物件所分析的[筆劃](/previous-versions/ms552701(v=vs.100))集合會包含在分隔物件的 [[筆觸](/previous-versions/ms839422(v=msdn.10))] 屬性中。 當您在集合中加入或刪除時，分隔物件會動態分析筆劃集合。 如需分割物件之 [筆觸] 屬性的詳細資訊，請參閱 [使用筆劃集合](working-with-a-strokes-collection.md)。

[分割](/previous-versions/ms583616(v=vs.100))物件會使用辨識器內容來改善其辨識區段的分析，並產生手寫元素的辨識文字。 您可以使用分隔物件的 [RecognizerCoNtext](/previous-versions/ms839415(v=msdn.10)) 屬性來設定辨識器內容。 將筆劃指派給分隔物件之後，就無法變更 RecognizerCoNtext 屬性。 如需分割物件之 RecognizerCoNtext 屬性的詳細資訊，請參閱 [使用辨識器內容](working-with-a-recognizer-context.md)。

> [!Caution]  
> 在 managed 程式碼中，您必須在此物件上呼叫 [Dispose](/previous-versions/ms839450(v=msdn.10)) 方法，才能使其超出範圍。 這個物件會維護非受控資源。 依賴此物件的完成可能會導致應用程式中的記憶體流失和例外狀況。

 

 

 
