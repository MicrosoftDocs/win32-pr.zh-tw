---
title: 使用解壓縮的範例複製資料流程
description: 使用解壓縮的範例複製資料流程
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows媒體格式 SDK，複製資料流程
- Advanced Systems Format (ASF) ，複製資料流程
- ASF (Advanced Systems Format) ，複製資料流程
- 資料流程，使用解壓縮的資料進行複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e044d2a1d456c14c2e2d069e0a117ab6f6de218c062771da9c24bf887ddfdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848804"
---
# <a name="copying-streams-using-decompressed-samples"></a>使用解壓縮的範例複製資料流程

強烈建議您不要使用解壓縮的範例，將資料流程從一個檔案複製到另一個檔案。 解壓縮和 recompressing 範例的程式將會降低輸出的品質。 如果您需要解壓縮範例，然後將它們複製到另一個資料流程，您可能會遇到以品質為基礎的變數位元速率的一些困難 (VBR) 編碼的資料流程。

當編解碼器完成壓縮以品質為基礎的 VBR 串流時，它會記錄所產生內容的位元速率和緩衝區視窗。 當您讀取的檔案包含以品質為基礎的 VBR 編碼的資料流程時，從讀取器取得的設定檔將會注意位元速率和緩衝區視窗，以及最大的位元速率和最大緩衝區視窗。 設定檔中的這項設定通常表示位速率限制的可變位頻率資料流程。 如此一來，當您在寫入器上設定設定檔時，就會預期資料流程的前置處理行程，因為位速率限制的 VBR 資料流程需要雙向編碼。 您應該將資料流程視為位速率受限的 VBR 資料流程，並傳遞範例進行前置處理。 因為您使用在特定品質層級編碼內容之後所傳回的值，所以這些值代表所需的品質等級。 當然，重新編碼的輸出品質也會因為重新編碼的結果而稍微降級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將資料從一個檔案複製到另一個檔案**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**複製資料流程而不解壓縮資料**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




