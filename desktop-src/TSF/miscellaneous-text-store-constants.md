---
title: '其他文字存放區常數 (Textstor .h) '
description: 其他的文字存放區常數會設定文字存放區的特定屬性。
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55bfa06f7f0ebda1d572a4e637076de25c7a21ef4d273cdc2527ab6481393404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952096"
---
# <a name="miscellaneous-text-store-constants"></a>其他文字存放區常數

其他的文字存放區常數會設定文字存放區的特定屬性。



| 常數/值                                                                                                                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_預設 \_ 選項**</dt> <dt> ( ( ULONG ) -1 )</dt> </dl> | 如果 [ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)的 *ulIndex* 參數設定為此值，則會取得預設的選取專案。<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_GEA \_ HIDDEN**</dt> <dt> ( 0x1 )</dt> </dl>                              | 如果 [ITextStoreAnchor：： GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)的 *dwFlags* 參數設定為此值，則内嵌物件可以位於隱藏文字內。<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_GTA \_ HIDDEN**</dt> <dt> ( 0x1 )</dt> </dl>                              | 未使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ST \_ 更正**</dt> <dt> ( 0x1 )</dt> </dl>                     | 如果 [ITextStoreACP：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)、 [ITextStoreAnchor：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)或 [ITextStoreACPSink：： OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)的 *dwFlags* 參數設定為此值，則文字會是 () 更正現有內容的轉換，而且會保留任何 (中繼資料) 的特殊文字標記資訊，例如 .wav 檔資料或語言識別項。<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_TC \_ 更正**</dt> <dt> ( 0x1 )</dt> </dl>                     | 如果 [ITextStoreAnchorSink：： OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)的 *dwFlags* 參數設定為此值，則文字會是 () 更正現有內容的轉換，而且會保留任何 (中繼資料) 的特殊文字標記資訊，例如 .wav 檔案資料或語言識別項。<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_VCOOKIE \_ NUL**</dt> <dt> ( 0xffffffff )</dt> </dl>                    | 由 TSF 在內部使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink：： OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[其他架構常數](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





