---
title: 'GXFPF_ 常數 (Textstor) '
description: GXFPF \_ \ 常數會根據相對於字元周框方塊的點螢幕座標，來指定要傳回的字元位置。
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464705"
---
# <a name="gxfpf_-constants"></a>GXFPF \_ \* 常數

GXFPF \_ \* 常數會根據相對於字元周框方塊的點螢幕座標，來指定要傳回的字元位置。



| 常數/值                                                                                                                                                                                                                                | Description                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**GXFPF \_四捨五入 \_ 最接近**</dt>的 <dt> ( 0x1 )</dt> </dl> | 如果點的螢幕座標包含在字元周框方塊中，則傳回的字元位置是最接近該點螢幕座標的周框邊緣。<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**GXFPF \_最接近**</dt>的 <dt> ( 0x2 )</dt> </dl>                    | 如果點的螢幕座標未包含在字元周框方塊中，則會傳回最接近的字元位置。<br/>                                                      |



## <a name="remarks"></a>備註

[ITextStoreACP：： GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)和 [ITfCoNtextOwner：： GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)方法的 *dwflags* 參數會使用這些常數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITextStoreACP：： GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITfCoNtextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





