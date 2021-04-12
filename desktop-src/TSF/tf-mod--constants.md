---
title: 'TF_MOD_ 常數 (Msctf) '
description: TF \_ MOD \_ \ 常數會指定 tf PRESERVEDKEY 結構中的索引鍵修飾詞 \_ 。
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025057"
---
# <a name="tf_mod_-constants"></a>TF \_ MOD \_ \* 常數

TF \_ MOD \_ \* 常數會指定[TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)結構中的索引鍵修飾詞。



| 常數/值                                                                                                                                                                                                                                                      | Description                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <dt>**TF \_MOD \_ ALT**</dt> <dt>0x0001</dt> </dl>                                                   | 按下 ALT 鍵的任一個<br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <dt>**TF \_MOD \_ 控制項**</dt> <dt>0x0002</dt> </dl>                                       | 按下 CTRL 鍵的任一個<br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <dt>**TF \_MOD \_ 移位**</dt> <dt>0x0004</dt> </dl>                                             | 按下 SHIFT 鍵的任一個<br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <dt>**TF \_MOD \_ RALT**</dt> <dt>0x0008</dt> </dl>                                                | 按下右邊的 ALT 鍵<br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <dt>**TF \_MOD \_ RCONTROL**</dt> <dt>0x0010</dt> </dl>                                    | 按下右 CTRL 鍵<br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <dt>**TF \_MOD \_ RSHIFT**</dt> <dt>0x0020</dt> </dl>                                          | 按下右移鍵<br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <dt>**TF \_MOD \_ LALT**</dt> <dt>0x0040</dt> </dl>                                                | 左 ALT 鍵已按下<br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <dt>**TF \_MOD \_ LCONTROL**</dt> <dt>0x0080</dt> </dl>                                    | 按下 CTRL 鍵<br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <dt>**TF \_MOD \_ LSHIFT**</dt> <dt>0x0100</dt> </dl>                                          | 已按下左 SHIFT 鍵<br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <dt>**TF \_\_在 \_ KEYUP 0x0200 上的 MOD**</dt> <dt></dt> </dl>                                   | 釋放金鑰時，就會引發此事件。 如果沒有這個旗標，則會在按下按鍵時引發事件。<br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <dt>**TF \_MOD \_ 忽略 \_ 所有 \_ 修飾**</dt>詞 <dt>0x0400</dt> </dl> | 會忽略 ALT、CTRL 和 SHIFT 鍵的狀態。 這表示當按下虛擬機器碼時，就會引發事件，無論按下哪個輔助按鍵。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





