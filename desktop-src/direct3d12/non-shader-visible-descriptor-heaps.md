---
title: 非著色器可見描述元堆積
description: 部分描述元堆積無法透過描述項資料表來參考著色器，但存在於記錄命令清單之前，或因為不需要著色器可見的堆積，以協助應用程式暫存描述項。
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343453"
---
# <a name="non-shader-visible-descriptor-heaps"></a>非著色器可見描述元堆積

部分描述元堆積無法透過描述項資料表來參考著色器，但存在於記錄命令清單之前，或因為不需要著色器可見的堆積，以協助應用程式暫存描述項。

-   [非可見的視圖](#non-visible-views)
-   [總結](#summary)
-   [相關主題](#related-topics)

## <a name="non-visible-views"></a>非可見的視圖

所有描述元堆積（包括先前所述的著色器可存取描述元），都可以由 CPU 和/或命令清單操作，這取決於應用程式針對描述項堆積所選取的記憶體集區和 CPU 存取屬性。

若為 [著色器可見的描述](shader-visible-descriptor-heaps.md)項堆積，則在暫存這些描述元時拒絕著色器存取的明顯原因。 然後，這些堆積會顯示為著色器，並在命令清單執行時透過描述項資料表來存取。 但是，不需要暫存著色器可見的堆積，而是可以直接填入。

其他描述元會將其內容直接記錄到命令清單中，以系結至管線。 這些描述項只提供在命令清單記錄時間轉譯 view 參數。 這些堆積一律為非著色器的可見度，並包含下列各項。

-    (RTVs) 呈現目標視圖
-   深度樣板視圖 (Dsv) 

索引緩衝區視圖 (IBVs) 、頂點緩衝區視圖 (VBVs) ，以及串流輸出視圖 (SOVs) 直接傳遞給 API 方法，所以沒有特定的堆積類型。

在記錄至命令清單之後 (呼叫（例如 [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)），例如) 用來保存此呼叫之描述項的記憶體可立即在呼叫後重複使用。

即使是描述中繼資料表，也有一些選項可讓應用程式選擇在命令清單記錄中記錄資料表內容 (而不是在執行) 時對資料表指標進行取值。

## <a name="summary"></a>總結



|                   | 著色器可見、僅限 CPU 寫入                                   | 非著色器可見、CPU 讀取/寫入                                       |
|-------------------|------------------------------------|----------------------------------------|
| **CBV，SRV，UAV** | 是                                | 是                                    |
| **採樣**       | 是                                | 是                                    |
| **RTV**           | 否                                 | 是                                    |
| **DSV**           | 否                                 | 是                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述元堆積](descriptor-heaps.md)
</dt> </dl>

 

 




