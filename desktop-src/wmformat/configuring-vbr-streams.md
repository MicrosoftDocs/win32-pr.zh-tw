---
title: 設定 VBR 資料流程
description: 設定 VBR 資料流程
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- 串流，設定 VBR 資料流程
- '資料流程、變數位元速率 (VBR) '
- 變數位速率 (VBR) ，資料流程
- VBR (變數位速率) ，資料流程
- 資料流程，IWMPropertyVault 介面
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3434ec508afdca9637b300ac83777cca33e0e59566b01c7fb027d547f39302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655966"
---
# <a name="configuring-vbr-streams"></a>設定 VBR 資料流程

您可以使用變數位元速率 (VBR) 編碼來產生本機檔案的高品質串流，或進行下載和播放。 有三個適用于 VBR 的選項：品質型 (一次傳遞) 、未受限制的 (雙通路) ，以及限制 (雙通路) 。 如需有關 VBR 編碼類型的詳細資訊，請參閱 [變數位元速率 (VBR) 編碼](variable-bit-rate--vbr--encoding.md)。

您可以使用 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) 介面設定屬性，以在設定檔中設定 VBR 編碼。 下表說明用來設定 VBR 編碼的屬性。



| 屬性                     | 描述                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| **g \_ wszVBREnabled**         | 布林值。 設定為 True 以使用 VBR 編碼。                                                   |
| **g \_ wszVBRQuality**         | **DWORD** 值。 設定為所需的品質層級 (1 到 100) 以品質為基礎的 VBR 編碼。      |
| **g \_ wszVBRBitrateMax**      | **DWORD** 值。 針對限制的 VBR 編碼，設定為最大位元速率（以每秒位數為單位）。   |
| **g \_ wszVBRBufferWindowMax** | **DWORD** 值。 針對受限的 VBR 編碼設定為最大緩衝區視窗（以毫秒為單位）。 |



 

下列各節說明如何使用不同類型的變數位速率編碼。



| 區段                                                              | 描述                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [設定 Quality-Based VBR](to-configure-quality-based-vbr.md) | 描述如何根據靜態品質等級來使用變數位元速率編碼。                                   |
| [設定未受限制的 VBR](to-configure-unconstrained-vbr.md) | 描述如何根據目標平均位元速率（沒有明確的尖峰值）來使用變數位元速率編碼。 |
| [設定限制的 VBR](to-configure-constrained-vbr.md)     | 描述如何根據目標平均位元速率和明確尖峰值，來使用變數位元速率編碼。     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> </dl>

 

 




