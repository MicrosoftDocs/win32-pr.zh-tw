---
title: 'TS_SD_ 常數 (Textstor) '
description: TS \_ SD \_ \ 常數描述應用程式在執行時間所使用的動態檔狀態。
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991122"
---
# <a name="ts_sd_-constants"></a>TS \_ SD \_ \* 常數

TS \_ SD \_ \* 常數描述應用程式在執行時間所使用的動態檔狀態。



| 常數/值                                                                                                                                                                                                                                              | Description                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <dt>**TS \_SD \_ READONLY**</dt> <dt> ( 0x1 )</dt> </dl>                              | 檔是唯讀的，而且無法修改。<br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <dt>**TS \_SD \_**</dt> <dt>)  ( 0x2</dt>載入 </dl>                                 | 檔正在載入，而且可能不完整。<br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <dt>**TS \_SD \_ MASKALL**</dt> <dt> ( ts \_ sd \_ READONLY \| ts \_ sd \_ ) 的載入</dt> </dl> | 檔是唯讀和載入的。<br/>       |



## <a name="remarks"></a>備註

[TS \_ 狀態](/windows/desktop/api/Textstor/ns-textstor-ts_status)結構的 **dwDynamicFlags** 成員會使用這些常數。

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

[TS \_ 狀態](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[TF \_ SD \_ \* 常數](tf-sd--constants.md)
</dt> </dl>

 

 





