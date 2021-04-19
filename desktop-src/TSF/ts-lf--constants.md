---
title: 'TS_LF_ 常數 (Textstor) '
description: TS \_ LF \_ \ 常數會指定檔鎖定的類型。
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969133"
---
# <a name="ts_lf_-constants"></a>TS \_ LF \_ \* 常數

TS \_ LF \_ \* 常數會指定檔鎖定的類型。



| 常數/值                                                                                                                                                                                                                    | Description                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <dt>**TS \_LF \_ 同步**</dt> <dt> ( 0x1 )</dt> </dl>                | 如果此旗標與其他旗標合併，則檔具有同步鎖定。<br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <dt>**TS \_LF \_ READ**</dt> <dt> ( 0x2 )</dt> </dl>                | 檔有唯讀鎖定，無法修改。<br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <dt>**TS \_LF \_ READWRITE**</dt> <dt> ( 0x6 )</dt> </dl> | 檔具有讀取/寫入鎖定，而且可以修改。<br/>                        |



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

[檔鎖定](document-locks.md)
</dt> <dt>

[ITextStoreACP：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor：： RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink：： OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





