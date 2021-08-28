---
description: 本節說明如何撰寫自訂媒體基礎轉換 (MFT) 。
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: 撰寫自訂的 MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c113867c719fc9c8512b5b0e1172ee0694e3905
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471654"
---
# <a name="writing-a-custom-mft"></a>撰寫自訂的 MFT

本節說明如何撰寫自訂媒體基礎轉換 (MFT) 。

## <a name="mft-checklist"></a>MFT 檢查清單

當您執行自訂的 MFT 時，請使用下列檢查清單來判斷需求：




| | |所有 MFTs |所有 MFTs 都必須執行 <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>。<br /> 下列主題提供有關如何執行此介面的詳細資訊：<ul><li><a href="basic-mft-processing-model.md">基本 MFT 處理模型</a></li><li><a href="time-stamps-and-durations.md">時間戳記和持續時間</a></li><li><a href="handling-stream-changes.md">處理資料流程變更</a></li></ul><br /> | |編碼器和解碼器 |需求：請參閱 <a href="implementing-a-codec-mft.md">執行編解碼器 MFT</a>。<br /> 建議：執行 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> 或 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>，以支援服務品質 (QoS) 通知。<br /> | |影片解碼器和視頻處理器 |選用：支援 DirectX Video 加速。<br /><ul><li><a href="direct3d-aware-mfts.md">Direct3D 感知 MFTs</a></li><li><a href="supporting-dxva-2-0-in-media-foundation.md">媒體基礎中支援 DXVA 2。0</a></li></ul> | |硬體編解碼器 |請參閱 <a href="hardware-mfts.md">硬體 MFTs</a>。 | |讓應用程式可探索您的 MFT ... |請參閱 <a href="registering-and-enumerating-mfts.md">註冊和列舉 MFTs</a>。 | |非同步資料處理 |預設的 MFT 模型會使用同步 (封鎖) 呼叫來處理資料。 針對某些 MFTs，非同步處理可能更有效率。 但是，它也比較複雜。<br /> 如需詳細資訊，請參閱 <a href="asynchronous-mfts.md">非同步 MFTs</a>。<br /> | |速率控制、訣竅模式或反向播放 |請參閱 <a href="implementing-rate-control.md">執行速率控制</a>。 | |如果您的 MFT 建立執行緒 ... |執行 <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> 介面。 | |如果您的 MFT 有授許可權制 ... |請考慮使用「使用欄位」機制。 請參閱 <a href="field-of-use-restrictions.md">使用限制的領域</a>。 | |如果您正在移植現有的 DirectX 媒體物件 (DMO) ... |請參閱<a href="comparison-of-mfts-and-dmos.md">MFTs 和 DMOs 的比較</a>。 | 




 

本節包含下列主題：

-   [時間戳記和持續時間](time-stamps-and-durations.md)
-   [處理資料流程變更](handling-stream-changes.md)
-   [執行編解碼器 MFT](implementing-a-codec-mft.md)
-   [Direct3D 感知 MFTs](direct3d-aware-mfts.md)
-   [硬體 MFTs](hardware-mfts.md)
-   [編解碼器的優點](codec-merit.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 




