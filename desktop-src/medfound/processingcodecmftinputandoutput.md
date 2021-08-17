---
description: 處理編解碼器 MFT 輸入和輸出
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: 處理編解碼器 MFT 輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cbec9b92ae11d8f1f3722f2cb2540a5b5b01bb5d680e448d298a36ec682ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101837"
---
# <a name="processing-codec-mft-input-and-output"></a>處理編解碼器 MFT 輸入和輸出

當您設定了 MFT 的輸入類型和輸出類型時，就可以開始處理資料範例。 您可以使用 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法，將範例傳遞給 MFT 以進行處理，然後藉由呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)來取得已處理的範例。 您應該為所有傳遞的輸入樣本設定正確的時間戳記和持續時間。 時間戳記並非絕對必要，但有助於維護音訊/影片同步處理。 如果您沒有範例的時間戳記，最好不要將其保留，而不是使用不確定的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



