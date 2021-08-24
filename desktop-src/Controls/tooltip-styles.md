---
title: '工具提示樣式 (CommCtrl .h) '
description: 此區段會列出與工具提示控制項搭配使用的控制項樣式。
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dddd890f8bf3aad35d20ec2eabcbe34f89b3ef262fbe30586f9a0a893f85e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751019"
---
# <a name="tooltip-styles"></a>工具提示樣式

此區段會列出與工具提示控制項搭配使用的控制項樣式。



| 常數                                                                                                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**TTS \_ ALWAYSTIP**</dt> </dl>                | 指出工具提示控制項出現時，即使工具提示控制項的主控視窗處於非使用中狀態，也會出現工具提示控制項。 若未使用此樣式，則只有當工具的擁有者視窗為使用中時，工具提示才會出現。<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**TTS \_ 氣球**</dt> </dl>                      | [版本 5.80](common-control-versions.md)。 指出工具提示控制項具有具有圓角的卡通「球標」的外觀，以及指向該專案的詞幹。 <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**TTS \_ 關閉**</dt> </dl>                            | 在工具提示上顯示 [ **關閉** ] 按鈕。 只有當工具提示具有 TTS \_ 氣球樣式和標題時有效，請參閱 [**TTM \_ SETTITLE**](ttm-settitle.md)。<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ NOANIMATE**</dt> </dl>                | [版本 5.80](common-control-versions.md)。 停用 Windows 98 和 Windows 2000 系統上的滑動工具提示動畫。 舊版系統會忽略這個樣式。<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS \_ NOFADE**</dt> </dl>                         | [版本 5.80](common-control-versions.md)。 停用淡化工具提示動畫。 <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**TTS \_ NOPREFIX**</dt> </dl>                   | 防止系統從字串中移除連字號字元，或在定位字元處終止字串。 若未使用此樣式，系統會自動去除連字號字元，並在第一個定位字元結束字串。 這可讓應用程式使用與功能表項目相同的字串，以及工具提示控制項中的文字。<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**TTS \_ USEVISUALSTYLE**</dt> </dl> | 使用主題超連結。 主題將會定義工具提示中任何連結的樣式。 此樣式一律需要 \_ 設定 TTF PARSELINKS。 <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>備註

\_ \_ 無論您是在建立控制項時指定它們，工具提示控制項一律會有 ws POPUP 和 ws EX \_ 工具視窗視窗樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





