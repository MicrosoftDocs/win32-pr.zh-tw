---
title: '[語音命令] 視窗 (的 [先進字元選項] 視窗) '
description: 深入瞭解 [先進字元選項] 視窗，其提供選項讓使用者調整其與所有字元的互動。
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404355"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>[語音命令] 視窗 (的 [先進字元選項] 視窗) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

[先進的字元選項] 視窗提供選項讓使用者調整其與所有字元的互動。 例如，使用者可以停用語音輸入或變更輸入參數。 使用者也可以變更文字氣球的輸出設定。 這些設定會覆寫用戶端應用程式所設定的任何設定，或設定為字元定義的一部分。 您的應用程式無法變更或停用這些選項，因為這些選項適用于所有字元操作的一般使用者喜好設定。 但是，伺服器會在使用者變更並套用選項時，通知您的應用程式 ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) 。 您也可以使用視窗的 [**Visible**](visible-property.md)屬性來顯示或關閉視窗，並透過其 [**左上**](top-property.md)[**角屬性存取**](left-property.md)其位置。

除了支援字元的動畫之外，Microsoft Agent 還支援字元的音訊輸出。 這包括語音輸出和音效效果。 針對說出的輸出，伺服器會自動將字元的已定義嘴影像與輸出同步。 您可以選擇文字轉換語音 (TTS) 合成、錄製的音訊，或僅限文字氣球文字輸出。

 

 




