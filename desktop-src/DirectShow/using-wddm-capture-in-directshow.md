---
description: 在 DirectShow 中使用 WDDM Capture
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: 在 DirectShow 中使用 WDDM Capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992059"
---
# <a name="using-wddm-capture-in-directshow"></a>在 DirectShow 中使用 WDDM Capture

本主題適用于 Windows Vista 和更新版本。

有些視訊卡有整合的影片捕捉功能。 在這些卡片上，已捕捉的影片畫面會放在視訊記憶體中 (VRAM) 。 在 Windows Vista 之前，沒有標準的機制可處理畫面格保持在 VRAM 的狀態。 相反地，必須將資料複製到系統記憶體中，然後再將資料複製回 VRAM 以供顯示。 在 Windows Vista 中，DirectShow 現在支援一種機制，可讓整個處理管線的影片畫面保持 VRAM，從 capture 到顯示。

KsProxy 篩選器會藉由查詢 KSPROPERTY \_ 慣用 \_ 捕獲介面屬性的驅動程式，來判斷驅動程式是否支援 VRAM 介面捕捉 \_ 。  (此屬性記載于 Windows 驅動程式套件檔中。 ) 如果驅動程式支援 VRAM surface capture，KsProxy 會配置一種特殊類型的媒體範例，其中包含 Direct3D 介面的指標。

接下來，KsProxy 會判斷下游篩選器是否支援 DirectX Video 加速 (DXVA) 2.0，如下所示：

1.  KsProxy 會查詢 **IMFGetService** 介面的下游輸入 pin。
2.  如果釘選公開 **IMFGetService**，KsProxy 會針對 **IDirect3DDeviceManager** 介面呼叫 **IMFGetService：： GetService** 。 服務 identier 是 MR \_ VIDEO \_ 加速 \_ 服務。

這兩個介面都記載于媒體基礎 SDK 檔集內。

如果下游篩選器不支援 DXVA 2.0，則 KsProxy 會配置額外的系統記憶體緩衝區。 它會使用此緩衝區將影片畫面從 VRAM 複製到系統記憶體。 Media 範例的 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 方法會傳回這個系統記憶體緩衝區的指標。

但是，如果下游篩選器支援 DXVA 2.0，則 KsProxy 不會配置系統記憶體緩衝區。 在此情況下， **GetPointer** 方法會傳回 E \_ >notimpl。 相反地，下游篩選器應該會直接存取範例的 Direct3D 介面。 下游篩選器有兩種方式可取得介面的指標，兩者都是相等的：

-   查詢 **IMFGetService** 介面的範例，並針對 **IDirect3DSurface9** 介面呼叫 **GetService** 。 服務識別碼是 MR \_ 緩衝區 \_ 服務。
-   查詢 [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) 介面的範例，然後呼叫 [**IMediaSample2Config：： GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> </dl>

 

 



