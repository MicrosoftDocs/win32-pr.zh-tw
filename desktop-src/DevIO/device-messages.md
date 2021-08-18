---
description: 裝置訊息是通知應用程式和其他裝置變更事件功能的系統訊息。
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: 裝置訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a26666ab0f7675da02e70d53ffd8aec5040a0482a0a2cdc71279fcaeca8ca92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053507"
---
# <a name="device-messages"></a>裝置訊息

裝置訊息是通知應用程式和其他裝置變更事件功能的系統訊息。 當系統偵測到系統硬體有變更時，就會發生這些事件，例如當使用者將膝上型電腦停駐和取消停用，或是插入或移除裝置（例如 PCMCIA 卡）時。 裝置事件可能會在系統執行時，或在暫時擱置後系統繼續操作時發生。

為了確保應用程式在裝置無法使用時不會遺失資料，系統會監視硬體設定，並將裝置訊息傳送至應用程式，以通知這些變更，並讓他們有機會在變更發生前加以準備。

針對每個裝置事件，系統會將 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息廣播至所有應用程式。 在此訊息中， *wParam* 參數會識別 [裝置事件種類](device-event-types.md) ，而 *lParam* 參數是事件特定資料的指標。

 

 



