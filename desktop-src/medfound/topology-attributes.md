---
description: 拓撲屬性
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: 拓撲屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106998992"
---
# <a name="topology-attributes"></a>拓撲屬性

下列屬性適用于拓撲。



| 屬性                                                                                                | 描述                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ 拓撲 \_ DXVA \_ 模式](mf-topology-dxva-mode.md)                                                    | 指定拓撲載入器是否會啟用拓撲中的 Microsoft DirectX Video 加速 (DXVA) 。                                                                                                                         |
| [\_ \_ \_ \_ 不 \_ 允許使用 MF 拓撲動態變更](mf-topology-dynamic-change-not-allowed.md)                | 指定當資料流程的格式變更時，媒體會話是否嘗試修改拓撲。                                                                                                                           |
| [MF \_ 拓撲可 \_ 啟用 \_ XVP \_ 來 \_ 播放](mf-topology-enable-xvp-for-playback.md)                | 指定拓撲載入器是否會啟用轉碼視頻處理器 (XVP) 。 針對轉換，啟用硬體加速色彩轉換。                                                                                        |
| [MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型](mf-topology-enumerate-source-types.md)                         | 指定拓撲載入器是否列舉媒體來源所提供的媒體類型。                                                                                                                                     |
| [MF \_ 拓撲 \_ 硬體 \_ 模式](mf-topology-hardware-mode.md)                                            | 指定是否要在拓撲中包含以硬體為基礎的轉換。                                                                                                                                                            |
| [**MF \_ 拓撲 \_ 無 \_ MARKIN \_ MARKOUT**](mf-topology-no-markin-markout-attribute.md)                     | 指定管線是否修剪範例。                                                                                                                                                                                      |
| [MF \_ 拓撲 \_ 播放 \_ 畫面播放速率](mf-topology-playback-framerate.md)                                  | 指定監視器的重新整理頻率。                                                                                                                                                                                                |
| [MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度](mf-topology-playback-max-dims.md)                                   | 指定影片播放的目的地視窗大小。                                                                                                                                                                   |
| [**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)                                 | 指定目前區段內的拓撲開始時間，以 100-毫微秒單位表示。                                                                                                                                             |
| [**MF \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md)                                   | 指定目前區段內的拓撲停止時間，以 100-毫微秒單位表示。                                                                                                                                              |
| [**MF \_ 拓撲 \_ 解決 \_ 狀態**](mf-topology-resolution-status-attribute.md)                      | 指定嘗試解析拓撲的狀態。                                                                                                                                                                          |
| [\_ \_ \_ \_ \_ 展示參數上的 \_ MF 拓撲開始時間](mf-topology-start-time-on-presentation-switch.md) | 指定在第一個簡報之後排入的簡報開始時間。                                                                                                                                           |
| [MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化](mf-topology-static-playback-optimizations.md)           | 啟用影片管線中的靜態優化。                                                                                                                                                                                |
| [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)                                | 包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，用來將具有使用規定限制的 MFT 解除鎖定。 如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 



