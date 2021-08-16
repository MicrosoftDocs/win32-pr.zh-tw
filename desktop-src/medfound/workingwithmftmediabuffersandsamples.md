---
description: 使用 MFT 媒體緩衝區和範例
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: 使用 MFT 媒體緩衝區和範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964f1c2f2a5fd5f92d5af87213c6977fc51bee76caf3a281861788e2a2fb922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736449"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>使用 MFT 媒體緩衝區和範例

編解碼器 MFTs 使用媒體緩衝區和範例來回傳遞媒體資料。

媒體緩衝區是管理記憶體區塊的 COM 物件，通常是用來保存媒體資料。 當資料傳遞至或從 MFT 傳遞時，一律會以媒體緩衝區的形式傳遞。

所有媒體緩衝區都會公開 **IMFMediaBuffer** 介面。 此介面是針對任何類型的資料所設計。 包含影片資料的緩衝區通常也會公開 **IMF2DBuffer**。

媒體緩衝區的大小上限是配置給緩衝區的記憶體數量。 若要尋找大小上限，請呼叫 **IMFMediaBuffer：： GetMaxLength**。 在任何時間點，媒體緩衝區也都有目前的長度，也就是緩衝區中的有效資料量，範圍從零個位元組到最大的大小。 若要取得目前的長度，請呼叫 **IMFMediaBuffer：： GetCurrentLength**。 建立緩衝區時，目前的長度為零。 如果您將資料寫入緩衝區，請呼叫 **IMFMediaBuffer：： SetCurrentLength** 來更新目前的長度。

若要存取緩衝區中的記憶體，請呼叫 **IMFMediaBuffer：： Lock**。 這個方法會傳回記憶體區塊開頭的指標。 當您使用指標完成時，請呼叫 **IMFMediaBuffer：： Unlock**。 **鎖定** 方法不是執行緒同步處理機制;它不保證其他執行緒無法存取緩衝區。 **鎖定** 方法是用來確保在您呼叫 **解除鎖定** 方法之前，存取的記憶體會保持有效。

媒體基礎 SDK) 內容中 (的媒體範例物件，是包含零或多個緩衝區的已排序清單的物件。 媒體範例會公開 **IMFSample** 介面。

若要建立新的範例，請呼叫 **MFCreateSample** 函數。 一開始，範例的緩衝區清單是空的。 若要在清單結尾加入緩衝區，請呼叫 **IMFSample：： AddBuffer**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> <dt>

[使用編解碼器 MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



