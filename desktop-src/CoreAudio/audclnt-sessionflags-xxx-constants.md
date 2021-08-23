---
description: AUDCLNT \_ SESSIONFLAGS \_ XXX 常數表示與資料流程相關聯之音訊會話的特性。
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: 'AUDCLNT_SESSIONFLAGS_XXX 常數 (Audiosessiontypes) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15423d24d48a98b69c4ab1651941fba639885c03e27cf9df8b1834aab830bb6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018496"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>AUDCLNT \_ SESSIONFLAGS \_ XXX 常數

AUDCLNT \_ SESSIONFLAGS \_ XXX 常數表示與資料流程相關聯之音訊會話的特性。 用戶端可以透過 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)方法的 *StreamFlags* 參數，在初始化資料流程期間指定這些選項。



| 常數/值                                                                                                                                                                                                                                                                                                                   | 描述                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt> </dl>                       | 當沒有相關聯的資料流程，並且擁有持有參考的會話控制物件時，會話就會過期。<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_SESSIONFLAGS \_ 顯示 \_ 隱藏**</dt> <dt>0x20000000</dt> </dl>                                     | 建立音訊會話時，音量控制項會隱藏在磁片區混音器使用者介面中。 如果與資料流程相關聯的會話已經存在， [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 會開啟資料流程，磁片區控制項就會顯示在磁片區混音器中。<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ DISPLAY \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt> </dl> | 在會話到期之後，音量控制會在磁片區混音器使用者介面中隱藏。 <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Audiosessiontypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心音訊常數](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




