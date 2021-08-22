---
title: '其他 TSF 文字服務常數 (Ctffunc .h) '
description: 下列值適用于文字服務。
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd4d9cdd73cd42512fe667b84867328c65f13fafa7281341eca7ba6379eef7d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476768"
---
# <a name="miscellaneous-tsf-text-service-constants"></a>其他 TSF 文字服務常數

下列值適用于文字服務。



| 常數/值                                                                                                                                                                                                                                                            | Description                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <dt>**TF \_MENUREADY**</dt> <dt>0x00000001</dt> </dl>                                                | 目前無法使用。<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <dt>**TF \_PROPUI \_ 狀態 \_ SAVETOFILE**</dt> <dt>0x00000001</dt> </dl> | 可以序列化屬性。 如果此值不存在，就無法序列化屬性。 此值會搭配 [ITfFnPropertyUIStatus：： GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) 和 [ITfFnPropertyUIStatus：： SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)一起使用。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Ctffunc。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctffunc .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITfFnPropertyUIStatus：： GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[ITfFnPropertyUIStatus：： SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





