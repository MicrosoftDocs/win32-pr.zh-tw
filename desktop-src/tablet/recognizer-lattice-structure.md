---
description: 為了與 Windows Vista 和 Windows XP Tablet PC Edition 一起使用而建立的辨識器會使用一組結構，其中每個結構都稱為 >lattice，可將辨識結果傳遞回 Tablet PC 平臺程式庫。
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: 辨識器 >lattice 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5610d60428bd3259672f43e45efa59c25f78b7ddc5909c363610eaf08520e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716012"
---
# <a name="recognizer-lattice-structure"></a>辨識器 >lattice 結構

為了與 Windows Vista 和 Windows XP Tablet PC Edition 一起使用而建立的辨識器會使用一組結構，其中每個結構都稱為 >lattice，可將辨識結果傳遞回 Tablet PC 平臺程式庫。 Tablet PC 平臺接著會將這些結構中的資訊複製到 [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件、 [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) 集合和 [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) 物件中。

當平臺呼叫 [HRECOCONTEXT](hrecocontext-handle.md)控制碼上的 [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)函式時，辨識器應該會傳回 >lattice 的指標。

本節將詳細說明 >lattice 結構。 如需辨識器和相關概念的總覽，請參閱 [關於手寫辨識](about-handwriting-recognition.md)。

## <a name="the-need-for-a-lattice"></a>>lattice 的需求

辨識器可能會有數種方式可將一組筆墨筆觸分成辨識區段。 辨識器用來作為辨識區段的內容，取決於辨識器的類型。 英文語言辨識器通常會使用單字作為辨識區段。 其他辨識器可能會使用字元、圖形或手勢作為辨識區段。 >Lattice 結構的彈性可讓您以邏輯方式管理大量的辨識結果，這些結果可結合在複雜的關聯性中。

就內部而言，辨識器會使用 >lattice 來保存指定筆墨的基本識別單位。 >Lattice 也會保留合併結果的分數或信賴等級。 此外，>lattice 會將區段對應儲存至原始筆墨筆劃。

>Lattice 結構定義于 RecTypes .h 標頭檔中。 >Lattice 結構包含下列結構：

-   [**辨識 \_ >LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**辨識 \_ >LATTICE 資料 \_ 行**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**辨識 \_ >LATTICE \_ 元素**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**辨識 \_ >LATTICE \_ 屬性**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**辨識 \_ >LATTICE \_ 屬性**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>>Lattice 元件

下列範例會使用「一起」一字的筆觸，如下圖所示。 在範例中，會將區段評估為一或多個單字。 數位代表要評估之區段中的個別筆劃。 請注意，每個 "t" 字元都包含兩個筆劃。

!["合" 單字的筆劃](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

>Lattice 是由一或多個資料行所組成，每個區段各一個資料行。 每個資料行依次包含一或多個元素。 專案會保留不同的辨識替代專案。 如需資料行的詳細資訊，請參閱 [**辨識 \_ >lattice 資料 \_ 行**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) 結構。 如需元素的詳細資訊，請參閱 [**辨識 \_ >lattice \_ 元素**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) 結構。

評估上一個範例中所示的筆墨範例時，辨識器可能會傳回單一區段。 在此情況下，>lattice 包含具有單一元素的單一資料行。

更複雜的範例會在辨識器評估筆墨樣本時自行呈現，並產生每個區段的多個區段和多個替代項。

辨識替代項的數目可能會錯開，即使是小型筆墨範例也是如此。 例如，"t o g e t h e r" 可能產生下列結果：

-   「取得她」 (再加上每個字的替代專案) 
-   「收集」 (再加上每個字組的替代項) 
-   「給她」 (再加上每個字的替換) 
-   「一起」 (加上單字的替代項) 

在此情況下，辨識器可能會建立下列 >lattice 結構。

![「一起」一字的 >lattice 結構](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> 每個資料行都有相同的筆劃順序，因為它們全都參考相同的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。

 

 

 
