---
title: 設定任意資料流程類型
description: 設定任意資料流程類型
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- 資料流程，設定任意資料流程類型
- 編解碼器，設定任意資料流程類型
- 資料流程，GenProfile
- 編解碼器、GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965794"
---
# <a name="configuring-arbitrary-stream-types"></a>設定任意資料流程類型

大部分的任意串流類型只需要位元速率、緩衝區視窗，以及 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構中適當的主要媒體類型。 不過，有些任意類型需要進行額外的設定。

如果您在設定資料流程時遇到問題，請參閱此 SDK 隨附的範例應用程式（稱為 GenProfile）。 GenProfile 中定義的程式庫包含包含所有資料流程類型的程式碼。 如需 GenProfile 和其他範例的詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

下列各節說明如何設定任意的資料流程類型。



| 區段                                                                                                                                        | 描述                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [設定腳本資料流程](configuring-script-streams.md)                                                                                   | 描述如何設定腳本資料流程。                                                  |
| [設定檔案傳輸資料流程](configuring-file-transfer-streams.md)                                                                     | 說明如何設定檔案傳輸串流。                                           |
| [設定 Web 資料流程](configuring-web-streams.md)                                                                                         | 描述如何設定 Web 資料流程。                                                     |
| [設定文字資料流程](configuring-text-streams.md)                                                                                       | 描述如何設定文字串流。                                                    |
| [設定自訂任意資料流程](configuring-custom-arbitrary-streams.md)                                                               | 描述如何設定自訂任意資料流程類型的資料流程。                       |
| [計算任意資料流程的位元速率和緩衝區視窗值](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | 描述如何計算任意資料流程的位元速率和緩衝區視窗設定。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**任意資料流程**](arbitrary-streams.md)
</dt> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> </dl>

 

 




