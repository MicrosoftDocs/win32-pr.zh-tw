---
title: 音訊行和控制項查詢
description: 音訊行和控制項查詢
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- 多媒體音訊、混音器控制項
- 音訊、混音器控制項
- 音訊 mixers，音訊行
- 音訊行
- 音訊 mixers，控制項
- mixers，控制項
- mixers，音訊行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c417b55273ba3f7f96cd857979c73003ed0f88c2161e1c2ac14d934fddcff1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692108"
---
# <a name="audio-line-and-control-queries"></a>音訊行和控制項查詢

混音器服務提供用來決定音訊行、音訊行控制項及控制項詳細資料相關資訊的功能。 這些服務也會提供用來設定控制項詳細資料的功能。

您可以使用 [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) 函式來取得指定之音訊行的相關資訊。 此函式會針對指定的來源音訊行、目的地音訊行或行識別碼填滿 [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) 結構。 此結構包含目的地行號、音訊行中的通道數目，以及音訊行的簡短和完整名稱。

[**MixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)函式會取得一或多個與音訊行相關聯之控制項的一般資訊。 此函式會以指定的控制項或控制項的相關資訊填入 [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) 結構。 您可以使用 **mixerGetLineControls** 來取出下列其中一項的控制項屬性：

-   指定之原始程式列的所有控制項
-   指定之原始程式列的指定控制項
-   指定原始程式列之特定類別的第一個控制項

[**MixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)函式會抓取與音訊行相關聯之單一控制項的屬性。 此函式會以控制項目前的值填入 [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) 結構。

[**MixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)函式會使用 **MIXERCONTROLDETAILS** 結構的內容來設定指定之控制項的屬性。 在呼叫 **mixerSetControlDetails** 之前，您必須確定已填入此結構的所有成員。

 

 