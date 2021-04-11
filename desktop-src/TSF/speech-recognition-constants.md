---
title: '語音辨識常數 (Ctffunc .h) '
description: 下列值適用于語音辨識文字服務。
ms.assetid: ac433d15-738a-46ab-8f69-0fbfb6a8b654
topic_type:
- apiref
api_name:
- TF_DICTATION_ON
- TF_DICTATION_ENABLED
- TF_COMMANDING_ENABLED
- TF_COMMANDING_ON
- TF_SPEECHUI_SHOWN
- TF_SHOW_BALLOON
- TF_DISABLE_BALLOON
- TF_DISABLE_SPEECH
- TF_DISABLE_DICTATION
- TF_DISABLE_COMMANDING
api_location:
- Ctffunc.h
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04c9cfd340e79415d12202765a8db1578abba74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093964"
---
# <a name="speech-recognition-constants"></a>語音辨識常數

下列值適用于語音辨識文字服務。



| 常數/值                                                                                                                                                                                                                                         | Description                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DICTATION_ON"></span><span id="tf_dictation_on"></span><dl> <dt>**TF \_0x00000001 \_ 上的聽寫**</dt> <dt></dt> </dl>                   | 如果此位為1，則語音聽寫為使用中狀態。 否則，語音聽寫為非使用中。 這個值無法與中的 TF \_ 命令結合 \_ 。 搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。<br/> |
| <span id="TF_DICTATION_ENABLED"></span><span id="tf_dictation_enabled"></span><dl> <dt>**TF \_聽寫 \_ 已啟用**</dt> <dt>0x00000002</dt> </dl>    | 如果此位為1，則會啟用語音聽寫。 否則，就會停用語音聽寫。 搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。<br/>                                                       |
| <span id="TF_COMMANDING_ENABLED"></span><span id="tf_commanding_enabled"></span><dl> <dt>**TF \_命令 \_ 啟用**</dt>的 <dt>0x00000004</dt> </dl> | 如果此位為1，則會啟用語音命令。 否則，會停用語音命令。 搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。<br/>                                                           |
| <span id="TF_COMMANDING_ON"></span><span id="tf_commanding_on"></span><dl> <dt>**TF \_\_在0x00000008 上命令**</dt> <dt></dt> </dl>                | 如果此位為1，則語音命令為使用中。 否則，語音命令為非作用中。 此值不能與的 TF \_ 聽寫合併 \_ 。 搭配 GUID 區間 [ \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md) 區間使用。<br/>      |
| <span id="TF_SPEECHUI_SHOWN"></span><span id="tf_speechui_shown"></span><dl> <dt>**TF \_SPEECHUI \_ 顯示**</dt>的 <dt>0x00000010</dt> </dl>             | 目前無法使用。<br/>                                                                                                                                                                                                                              |
| <span id="TF_SHOW_BALLOON"></span><span id="tf_show_balloon"></span><dl> <dt>**TF \_顯示 \_ 氣球**</dt> <dt>0x00000001</dt> </dl>                   | 目前無法使用。 搭配 GUID 區間 [ \_ \_ 語音 \_ UI \_ 狀態](predefined-compartments.md) 區間使用。<br/>                                                                                                                              |
| <span id="TF_DISABLE_BALLOON"></span><span id="tf_disable_balloon"></span><dl> <dt>**TF \_停用 \_ 氣球**</dt>的 <dt>0x00000002</dt> </dl>          | 如果這個位為1，表示目前語音模式的氣球顯示已停用。 否則，會啟用目前語音模式的氣球顯示。 搭配 GUID 區間 [ \_ \_ 語音 \_ UI \_ 狀態](predefined-compartments.md) 區間使用。<br/>    |
| <span id="TF_DISABLE_SPEECH"></span><span id="tf_disable_speech"></span><dl> <dt>**TF \_停用 \_ 語音**</dt> <dt>0x00000001</dt> </dl>             | 如果此位為1，則會停用語音輸入。 否則，會啟用語音輸入。 搭配使用 [GUID 區間 \_ \_ 語音 \_ 停](predefined-compartments.md) 用區間。<br/>                                                                    |
| <span id="TF_DISABLE_DICTATION"></span><span id="tf_disable_dictation"></span><dl> <dt>**TF \_停用 \_ 聽寫**</dt> <dt>0x00000002</dt> </dl>    | 如果此位為1，則會停用語音聽寫。 否則，會啟用語音聽寫。 搭配使用 [GUID 區間 \_ \_ 語音 \_ 停](predefined-compartments.md) 用區間。<br/>                                                            |
| <span id="TF_DISABLE_COMMANDING"></span><span id="tf_disable_commanding"></span><dl> <dt>**TF \_停用 \_ 命令**</dt> <dt>0x00000004</dt> </dl> | 如果此位為1，則會停用 [語音] 命令。 否則，會啟用語音命令。 搭配使用 [GUID 區間 \_ \_ 語音 \_ 停](predefined-compartments.md) 用區間。<br/>                                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                                                                                         |
| 標頭<br/>                   | <dl> <dt>Ctffunc .h;</dt><dt>Msctf .h</dt> </dl>     |
| Idl<br/>                      | <dl> <dt>Ctffunc .idl;</dt><dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先定義的區間](predefined-compartments.md)
</dt> </dl>

 

 





