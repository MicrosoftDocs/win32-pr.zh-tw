---
title: 資料輸入和輸出
description: 資料輸入和輸出
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Windows Media Player 外掛程式、資料輸入和輸出
- 外掛程式、資料輸入和輸出
- 數位信號處理外掛程式、資料輸入和輸出
- DSP 外掛程式、資料輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31e7c6fba24451d65e59c3fb9f56ec6b1413be3d595530414c25c52964b9b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863668"
---
# <a name="data-input-and-output"></a>資料輸入和輸出

Windows Media Player 透過 Windows Media Player 所配置的輸入緩衝區，將音訊或影片資料提供給 DSP 外掛程式。 DSP 外掛程式會透過 Windows Media Player 也配置的輸出緩衝區，將已處理的資料傳回 Windows Media Player。 Windows Media Player 藉由呼叫外掛程式所執行的方法，管理在本身和 DSP 外掛程式之間傳遞資料的流程。 針對作為 DirectX 媒體物件 (DMO) 的外掛程式，此程式的運作方式如下：

1.  Windows Media Player 會呼叫 **IMediaObject：:P rocessinput**，將 **IMediaBuffer** 物件的指標傳遞至 DSP 外掛程式。
2.  DSP 外掛程式會保留輸入緩衝區物件的參考計數。 DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。
3.  Windows Media Player 會呼叫 **IMediaObject：:P rocessoutput**，將指標傳遞至 **DMO \_ 輸出 \_ 資料 \_ 緩衝區** (結構的陣列，其中包含到 DSP 外掛程式) 的輸出緩衝區。
4.  DSP 外掛程式會處理輸入緩衝區中的資料，然後將資料複製到適當的輸出緩衝區。 當緩衝區中的所有資料都已處理時，DSP 外掛程式會釋放輸入緩衝區物件的參考計數。 然後，DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。
5.  Windows Media Player 在輸出緩衝區中呈現內容。

針對作為媒體基礎轉換 (MFT) 的外掛程式，此程式的運作方式如下：

-   Windows Media Player 會呼叫 **IMFTransform：:P rocessinput**，將 **IMFSample** 介面物件的指標傳遞至 DSP 外掛程式。
    1.  DSP 外掛程式會保留 **IMFSample** 介面上的參考計數。 DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。
    2.  Windows Media Player 會呼叫 **IMFTransform：:P rocessoutput**，將指標傳遞至包含 DSP 外掛程式) 之輸出緩衝區的的 **MFT \_ 輸出 \_ 資料 \_ 緩衝區** 結構 (。
    3.  DSP 外掛程式會處理輸入緩衝區中的資料，然後將資料複製到適當的輸出緩衝區。 當緩衝區中的所有資料都已處理時，DSP 外掛程式會釋放輸入緩衝區物件的參考計數。 然後，DSP 外掛程式會傳回適當的成功或失敗 **HRESULT**。
    4.  Windows Media Player 在輸出緩衝區中呈現內容。

此程式會在外掛程式已啟用且 Windows Media Player 有要轉譯的內容時持續重複。

> [!Note]  
> 請勿撰寫將資料寫入輸入緩衝區或從輸出緩衝區讀取資料的程式碼。 不當存取資料緩衝區可能會產生非預期的結果。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




