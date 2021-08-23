---
description: 處理編解碼器 DMO 輸入和輸出
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: 處理編解碼器 DMO 輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3b159ea9e8a323a8e980b9dbba227aa2a62d76316b90e09f45592044091f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035086"
---
# <a name="processing-codec-dmo-input-and-output"></a>處理編解碼器 DMO 輸入和輸出

當您設定了 DMO 的輸入類型和輸出類型時，就可以開始處理資料範例。 您可以使用 **IMediaObject：:P rocessinput** 方法將範例傳遞至 DMO 進行處理，然後藉由呼叫 **IMediaObject：:P rocessoutput** 來取得已處理的範例。 您應該為所有傳遞的輸入樣本設定正確的時間戳記和持續時間。 時間戳記並非絕對必要，但有助於維護音訊/影片同步處理。 如果您沒有範例的時間戳記，最好不要將其保留，而不是使用不確定的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



