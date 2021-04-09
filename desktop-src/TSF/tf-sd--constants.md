---
title: 'TF_SD_ 常數 (Msctf) '
description: TF \_ SD \_ \ 常數描述檔狀態。
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093963"
---
# <a name="tf_sd_-constants"></a>TF \_ SD \_ \* 常數

TF \_ SD \_ \* 常數描述檔狀態。



| 常數/值                                                                                                                                                                                                                              | Description                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**TF \_SD \_ readonly**</dt> <dt> ( TS \_ SD \_ readonly )</dt> </dl> | 檔是唯讀的，而且無法修改。<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**TF \_\_**</dt> <dt> ( TS \_ SD \_ 載入 )</dt>的 SD 載入 </dl>     | 檔正在載入，而且可能不完整。<br/>    |



## <a name="remarks"></a>備註

[TF \_ 狀態](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))結構的 **dwDynamicFlags** 成員會使用這些常數。

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

[TF \_ 狀態](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[TS \_ SD \_ \* 常數](ts-sd--constants.md)
</dt> <dt>

[ITfCoNtextOwner：： GetStatus](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[ITfCoNtextOwnerServices::OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP：： GetStatus](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[ITfStatusSunk::OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

