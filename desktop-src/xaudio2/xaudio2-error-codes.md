---
description: XAudio2 XAudio2 方法所傳回的特定錯誤碼。
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: 'XAudio2 錯誤碼 (Xaudio2) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987919"
---
# <a name="xaudio2-error-codes"></a>XAudio2 錯誤碼

XAudio2 XAudio2 方法所傳回的特定錯誤碼。



| 常數/值                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_E \_ 不正確 \_ 呼叫**</dt> <dt>0x88960001</dt> </dl>                          | XAudio2 針對某些 API 使用錯誤所傳回的錯誤 (不正確呼叫，以及在執行時間應由標題處理的) 。  (完全肇因的 API 使用錯誤（例如不正確參數），會導致在零售組建中的偵測組建和未定義行為發生判斷提示，因此未定義任何錯誤碼。 ) <br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_E \_ XMA \_ 解碼器 \_ ERROR**</dt> <dt>0x88960002</dt> </dl>          | Xbox 360 XMA 硬體遭受無法復原的錯誤。<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_E \_ XAPO \_ 建立 \_ 失敗**</dt> <dt>0x88960003</dt> </dl> | 無法具現化效果。<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_E \_ 裝置 \_ 失效**</dt> <dt>0x88960004</dt> </dl>        | 音訊裝置無法透過插即用或其他事件來使用。<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>備註

### <a name="platform-requirements"></a>平台需求

Windows 10 (XAudio 2.9) ;Windows 8、Windows Phone 8 (XAudio 2.8) ;DirectX SDK (XAudio 2.7) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Xaudio2。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XAudio2：：常數](constants.md)
</dt> </dl>

 

 




