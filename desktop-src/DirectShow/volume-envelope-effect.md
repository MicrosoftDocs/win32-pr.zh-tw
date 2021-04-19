---
description: 音量信封效果
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: 音量信封效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983757"
---
# <a name="volume-envelope-effect"></a>音量信封效果

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

音量信封效果會在音訊串流上設定音量。

類別識別碼 (CLSID) ： {036A9790-C153-11D2-9EF7-006008039E37}

CLSID 變數名稱： CLSID \_ AudMixer

屬性



| 屬性 | 類型   | 預設 | 描述                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol      | double | 1.0     | 磁片區，以撰寫之磁片區的百分比表示。 您可以在一段時間內改變這個屬性值，以產生音訊淡化。 |



 

## <a name="remarks"></a>備註

時間軸中的每個物件最多隻能有一個音量信封效果。 在組合或群組中，會先套用音量信封，再套用任何其他音訊效果，而不論其優先順序為何。 在來源或播放軌中，會根據其優先順序套用磁片區效果。

 

 



