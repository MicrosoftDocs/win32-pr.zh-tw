---
title: Windows Vista 中的音訊 Mixers
description: Windows Vista 中的音訊 Mixers
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- 多媒體音訊，Windows Vista 音訊 mixers
- 音訊、Windows Vista 音訊 mixers
- 音訊 mixers，Windows Vista
- mixers，Windows Vista
- Windows Vista 音訊 mixers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104571208"
---
# <a name="audio-mixers-in-windows-vista"></a>Windows Vista 中的音訊 Mixers

從 Windows Vista 開始，某些混音器控制項是在軟體中執行，而不是在硬體中。 例如，磁片區控制項會使用 Windows 音訊會話 API 來執行 (WASAPI) 。 這些控制項不會直接影響硬體設定。 此外，它們與進程特定的音訊會話相關聯，因此變更會影響呼叫應用程式，但不會影響其他應用程式。

每個音訊端點裝置都有一個標準混音器版面配置，並在軟體中執行。

-   每個音訊轉譯端點都包含一個包含下列各項的目的地行：
    -   音量控制
    -   靜音控制
    -   來源行：波形-音訊輸出。
    -   來源行：音訊 CD。
-   每個音訊捕獲端點都包含一個目的地行，其中包含下列各項：
    -   音量控制
    -   靜音控制
    -   來源行：波形-音訊輸入。 元件類型取決於輸入裝置，例如麥克風。

每個原始程式列都包含音量控制項和靜音控制項。 下圖顯示呈現端點和捕捉端點的元件。

![預設混音器版面配置](images/mixer1.gif)

端點的所有控制項都可操作相同的基礎軟體控制項。 因此，如果您變更某個控制項的設定，您將會在其他控制項上收到控制項變更通知。  (參閱 [**MM \_ MIXM \_ 控制項 \_ 變更**](mm-mixm-control-change.md)。 ) 

此標準版面配置是為了與使用音訊混音器功能的現有應用程式相容。 新的應用程式應該避免使用這些功能。

 

 




