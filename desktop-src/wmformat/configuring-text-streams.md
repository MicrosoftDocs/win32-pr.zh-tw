---
title: 設定文字資料流程
description: 設定文字資料流程
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- 資料流程，設定文字資料流程
- 編解碼器，設定文字資料流程
- 文字資料流程，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462237"
---
# <a name="configuring-text-streams"></a>設定文字資料流程

文字資料流程基本上與自訂任意資料流程相同。 沒有與文字資料流程相關聯的設定資訊可識別文字編碼類型，因此寫入器物件無法驗證範例。

若要設定文字資料流程，您必須確定 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構包含 WMMEDIATYPE 文字的主要媒體類型 \_ 。 您也必須設定資料流程的位元速率和緩衝區視窗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**計算任意資料流程的位元速率和緩衝區視窗值**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定任意資料流程類型**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**文字資料流**](text-streams.md)
</dt> </dl>

 

 




