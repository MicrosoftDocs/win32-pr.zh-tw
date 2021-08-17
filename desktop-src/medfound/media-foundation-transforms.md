---
description: 媒體基礎轉換
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: 媒體基礎轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61057831383c808a3e05cbe2e9cd779b46522a7a3d52d379b936f27c549d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268698"
---
# <a name="media-foundation-transforms"></a>媒體基礎轉換

媒體基礎轉換 (MFTs) 提供用來處理媒體資料的一般模型。 MFTs 可用於 (Dsp) 的解碼器、編碼器和數位訊號處理器。 簡而言之，位於媒體來源和媒體接收器之間媒體管線中的任何事物，都是一個 MFT。

本節描述 MFT 程式設計模型，以及如何使用特定 MFTs 類型的建議（例如，解碼器）來執行 MFT。



| 主題                                                                    | 描述                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 MFTs](about-mfts.md)                                             | 提供 MFTs 的簡短總覽                                                                                                                                                                   |
| [基本 MFT 處理模型](basic-mft-processing-model.md)             | 更詳細地說明使用 MFT 處理資料的基本模型。                                                                                                                           |
| [非同步 MFTs](asynchronous-mfts.md)                               | 描述替代基本模型的非同步處理模型。<br/> Windows 7 中引進了非同步處理。 並非所有的 MFT 都支援此模型。<br/> |
| [註冊和列舉 MFTs](registering-and-enumerating-mfts.md) | 如何註冊 MFT 以及如何列舉登錄中的 MFTs。                                                                                                                                   |
| [使用限制領域](field-of-use-restrictions.md)               | 描述解除鎖定具有使用規定限制之 MFT 的機制。                                                                                                                    |
| [MFT 和 DMO 的比較](comparison-of-mfts-and-dmos.md)           | 摘要說明 MFTs 與 DMOs 之間的差異。                                                                                                                                                   |
| [撰寫自訂的 MFT](writing-a-custom-mft.md)                         | 撰寫自訂 MFT 的指導方針。                                                                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎管線](media-foundation-pipeline.md)
</dt> <dt>

[媒體基礎架構](media-foundation-architecture.md)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




