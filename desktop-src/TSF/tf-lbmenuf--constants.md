---
title: 'TF_LBMENUF_ 常數 (Ctfutb) '
description: TF \_ LBMENUF \_ \ 常數是在 ITfMenu AddMenuItem 方法中用來指定語言列中功能表項目的特性。
ms.assetid: f8f3f397-b84e-4635-b454-31369c679ce2
topic_type:
- apiref
api_name:
- TF_LBMENUF_CHECKED
- TF_LBMENUF_SUBMENU
- TF_LBMENUF_SEPARATOR
- TF_LBMENUF_RADIOCHECKED
- TF_LBMENUF_GRAYED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a056e9a758419965341b4d508db083fc8f31b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934330"
---
# <a name="tf_lbmenuf_-constants"></a>TF \_ LBMENUF \_ \* 常數

在 [ITfMenu：： AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)方法中，會使用 **TF \_ \_ \* LBMENUF* _ 常數來指定語言列中功能表項目的特性。



| 常數/值                                                                                                                                                                                                                                         | Description                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="TF_LBMENUF_CHECKED"></span><span id="tf_lbmenuf_checked"></span><dl> <dt>_ * TF \_LBMENUF \_ CHECKED * *</dt> <dt>0x01</dt> </dl>                | 已核取功能表項目。<br/>            |
| <span id="TF_LBMENUF_SUBMENU"></span><span id="tf_lbmenuf_submenu"></span><dl> <dt>**TF \_LBMENUF \_ 子功能表**</dt> <dt>0x02</dt> </dl>                | 功能表項目是子功能表。<br/>          |
| <span id="TF_LBMENUF_SEPARATOR"></span><span id="tf_lbmenuf_separator"></span><dl> <dt>**TF \_LBMENUF \_ 分隔符號**</dt> <dt>0x04</dt> </dl>          | 功能表項目為分隔符號。<br/>        |
| <span id="TF_LBMENUF_RADIOCHECKED"></span><span id="tf_lbmenuf_radiochecked"></span><dl> <dt>**TF \_LBMENUF \_ RADIOCHECKED**</dt> <dt>0x08</dt> </dl> | 功能表項目是一個單選標記。<br/> |
| <span id="TF_LBMENUF_GRAYED"></span><span id="tf_lbmenuf_grayed"></span><dl> <dt>**TF \_LBMENUF \_ 灰色**</dt> <dt>0x10</dt> </dl>                   | 功能表項目已停用。<br/>           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ctfutb。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)
</dt> </dl>

 

 





