---
description: 資源是 Direct3D 管線可以存取的記憶體中的區域。
ms.assetid: 24859fbc-b5e1-4963-baf8-4f083f41f39a
title: " (Direct3D 10) 的資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93448fadd14d1a0849c9b730d34030b70d42a8cbc0926743e7059e222a6ea9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567048"
---
# <a name="resources-direct3d-10"></a> (Direct3D 10) 的資源

資源是 Direct3D 管線可以存取的記憶體中的區域。 為了讓管線能夠有效率地存取記憶體，提供給管線 (例如輸入幾何、著色器資源、紋理等) 的資料必須儲存在資源中。 所有 Direct3D 資源衍生兩種類型的資源︰緩衝區或紋理。 每個管線階段可使用多達 128 種資源。

每個應用程式通常會建立許多資源。 資源的範例包括︰頂點緩衝區、索引緩衝區、常數緩衝區、紋理和著色器資源。 有幾個決定資源如何使用的選項。 您可以建立強類型或無類型的資源；您可以控制資源是否擁有讀取和寫入兩項存取權；您可以讓資源只供 CPU、GPU 或二者存取。 當然，會有速度和功能上的取捨，您若允許資源擁有更多的功能，您可預期的效能會更低。

因為應用程式通常會使用許多紋理，所以 Direct3D 也引進了材質陣列的概念，以簡化材質管理。 紋理陣列包含一個或多個紋理 (所有類型與大小均相同)，可以從應用程式中或由著色器編制索引。 紋理陣列可讓您使用具有多個索引的單一介面來存取許多紋裡。 您可以依需求建立任意數量的紋理陣列來管理不同紋理類型。

當您建立好應用程式將使用的資源之後，您會連接或繫結每個資源到將使用它們的管線階段。 您可以呼叫繫結 API 來完成這項作業，也就是指向資源。 由於有一個以上的管線階段可能需要存取相同的資源，因此 Direct3D 10 引進了資源檢視的概念。 檢視會辨識可存取的部分資源。 您可以建立 m 檢視或資源並將它們繫結到 n 管線階段，假設是您遵循共用資源的繫結規則 (若不這麼做，執行階段會在編譯時產生錯誤)。

資源檢視會提供存取資源的一般模型 (紋理、緩衝區等 ) 。 因為您可以使用檢視來告訴執行階段進行存取以及如何存取，所以資源檢視可讓您建立無類型的資源。 也就是您可以在編譯時建立指定大小的資源，然後在資源繫結到管線時宣告資源內的資料類型。 Views 會公開許多使用資源的新功能，例如，在著色器中讀取深度/樣板表面、在單一行程中產生動態 cubemaps，以及同時轉譯為磁片區的多個配量。

若要深入瞭解基本資源類型、材質陣列，以及如何建立和使用資源，請參閱下列其他主題：

-   [資源類型](d3d10-graphics-programming-guide-resources-types.md)
-   [選擇資源](d3d10-graphics-programming-guide-resources-choosing-basic.md)
-   [建立緩衝區資源](d3d10-graphics-programming-guide-resources-creating.md)
-   [建立材質資源](d3d10-graphics-programming-guide-resources-creating-textures.md)
-   [複製和存取資源資料](d3d10-graphics-programming-guide-resources-mapping.md)
-   [記憶體結構和 Views](d3d10-graphics-programming-guide-resources-access-views.md)
-   [區塊壓縮](d3d10-graphics-programming-guide-resources-block-compression.md)
-   [資源限制表](d3d10-graphics-programming-guide-resources-limits.md)
-   [座標系統](d3d10-graphics-programming-guide-resources-coordinates.md)
-   [浮點數規則](d3d10-graphics-programming-guide-resources-float-rules.md)
-   [資料類型轉換規則](d3d10-graphics-programming-guide-resources-data-conversion.md)
-   [對應舊版格式](d3d10-graphics-programming-guide-resources-legacy-formats.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



