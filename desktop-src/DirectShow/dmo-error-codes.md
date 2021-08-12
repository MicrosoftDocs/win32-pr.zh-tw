---
description: 下表包含適用于 Microsoft DirectX 媒體物件 (DMOs) 的錯誤碼。 這些錯誤碼會定義在標頭檔 Mediaerr 中。
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: 'DMO錯誤碼 (Mediaerr .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa8f45b8f9f61185adbcd79a354df8ab3e41471067b66179193b825a5e40651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653292"
---
# <a name="dmo-error-codes"></a>DMO錯誤碼

下表包含適用于 Microsoft DirectX 媒體物件 (DMOs) 的錯誤碼。 這些錯誤碼會定義在標頭檔 Mediaerr 中。



| 常數/值                                                                                                                                                                                                                                                  | 描述                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt> </dl> | 不正確資料流程索引。<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_E \_ INVALIDTYPE**</dt> <dt>0x80040202</dt> </dl>                      | 媒體類型無效。<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_E \_ 類型 \_ 未 \_ 設定**</dt> <dt>0x80040203</dt> </dl>                 | 媒體類型未設定。 一或多個資料流程需要媒體類型，才能執行這項作業。<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | 此資料流程無法接受資料。 您可能需要處理更多輸出資料;請參閱 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput)。<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_E \_ 類型 \_ 不 \_ 接受**</dt> <dt>0x80040205</dt> </dl>  | 媒體類型不被接受。<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_\_沒有 \_ 其他 \_ 專案**</dt> <dt>0x80040206</dt> </dl>              | 媒體類型索引超出範圍。<br/>                                                                                                                        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mediaerr。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DMO常數](dmo-constants.md)
</dt> </dl>

 

 




