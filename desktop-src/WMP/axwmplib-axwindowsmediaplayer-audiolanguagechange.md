---
title: AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件
description: 當目前的音訊語言變更時，就會發生 AudioLanguageChange 事件。 |AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40538dad18c4cb6767a034ab5d163f16d1822d9149e15c07ca1130f5eb17f30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582723"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件

當目前的音訊語言變更時，就會發生 AudioLanguageChange 事件。

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ AudioLanguageChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ AudioLanguageChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性   | 描述                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **langID** | **System.object** 唯一識別特定語言方言，稱為地區設定。<br/> |



 

## <a name="remarks"></a>備註

地區設定識別碼 (LCID) 可唯一識別特定語言方言，稱為地區設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





