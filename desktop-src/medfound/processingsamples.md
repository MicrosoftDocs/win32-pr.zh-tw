---
description: 處理編解碼器 SQL-DMO 輸入和輸出
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: 處理編解碼器 SQL-DMO 輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318740"
---
# <a name="processing-codec-dmo-input-and-output"></a>處理編解碼器 SQL-DMO 輸入和輸出

當您已設定了一類的輸入類型和輸出類型時，就可以開始處理資料範例。 您可以使用 **IMediaObject：:P rocessinput** 方法，將範例傳遞給 sql-dmo 以進行處理，然後藉由呼叫 **IMediaObject：:P rocessoutput** 來取得已處理的範例。 您應該為所有傳遞的輸入樣本設定正確的時間戳記和持續時間。 時間戳記並非絕對必要，但有助於維護音訊/影片同步處理。 如果您沒有範例的時間戳記，最好不要將其保留，而不是使用不確定的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



