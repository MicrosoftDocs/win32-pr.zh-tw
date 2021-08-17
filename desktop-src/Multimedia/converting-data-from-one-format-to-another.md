---
title: 將資料從一種格式轉換成另一種格式
description: 將資料從一種格式轉換成另一種格式
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- 音訊壓縮管理員 (的) 、轉換資料
- " (音效壓縮管理員) 、轉換資料"
- 進行中的範例，轉換資料
- 轉換資料
- acmStreamOpen 函式
- acmStreamSize 函式
- acmStreamPrepareHeader 函式
- acmStreamConvert 函式
- acmStreamUnprepareHeader 函式
- acmStreamClose 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ec1050066b92a356067085b491f5ddbf4bded47789c6e15a5187ea74c47c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144807"
---
# <a name="converting-data-from-one-format-to-another"></a>將資料從一種格式轉換成另一種格式

使用中的串流函數可支援資料格式轉換。 在 [資料類型] 中的轉換器會變更格式，但不會變更資料類型。 例如，轉換器模組可以將 44-kHz、16位資料變更為 44-kHz、8位的資料。

下列的執行的函數支援資料格式轉換。 它們會依照您通常使用它們的順序列出。

-   [**AcmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)函式會開啟轉換資料流程。
-   [**AcmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)函數會計算來源或目的緩衝區的適當大小。
-   [**AcmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)函式會準備要在轉換中使用的來源和目的地緩衝區。
-   [**AcmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)函式會將來源緩衝區中的資料轉換成目的地格式，將轉換的資料寫入目的地緩衝區。
-   [**AcmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)函式會清除 **acmStreamPrepareHeader** 所準備的來源和目的地緩衝區。 釋放來源和目的地緩衝區之前，您必須先呼叫此函數。
-   [**AcmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)函式會關閉轉換資料流程。

轉換資料時，請先識別來源格式，然後選擇目的地格式。 最簡單的方法是使用 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) 函式，此函式會顯示格式選擇對話方塊，並傳回使用者的格式選項。

當您知道來源和目的地格式時，您可以使用 [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) 來開啟轉換資料流程。 然後，您可以使用 [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) 函數來判斷適當的緩衝區大小。

下一步是使用 [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)準備要在轉換中使用的緩衝區。

若要執行轉換，請使用 [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) ，直到處理完所有緩衝區為止。 當轉換完成時，請使用 [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) 來清除緩衝區，然後使用 [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) 來關閉轉換資料流程。

 

 




