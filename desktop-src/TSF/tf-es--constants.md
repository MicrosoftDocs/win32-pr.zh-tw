---
title: 'TF_ES_ 常數 (Msctf) '
description: 以下是 ITfCoNtext RequestEditSession 方法所使用的常數。
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e8e85e110632275cea66d7e40e51fe889d4e28a46d6e5368de88d298b16676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950853"
---
# <a name="tf_es_-constants"></a>TF \_ ES \_ \* 常數

以下是 [ITfCoNtext：： RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) 方法所使用的常數。



| 常數/值                                                                                                                                                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <dt>**TF \_ES \_ ASYNCDONTCARE**</dt> <dt> ( 0 )</dt> </dl> | 編輯會話可能會以同步或非同步方式進行，由管理員自行決定。 管理員會嘗試排程同步編輯會話，以改善效能。 此值無法與 TF \_ es \_ ASYNC 或 tf \_ es \_ 同步值結合。<br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <dt>**TF \_ES \_ 同步**</dt> <dt> ( 0x1 )</dt> </dl>                          | 編輯會話必須是同步的，否則 (會有 TF \_ E 同步) 的要求將會失敗 \_ 。 此旗標只能在記載的情況下使用 (例如按鍵處理，) 應該會成功。 否則呼叫可能會失敗。 此值無法與 TF \_ es \_ ASYNCDONTCARE 或 tf \_ es \_ ASYNC 值結合。<br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <dt>**TF \_ES \_ READ**</dt> <dt> ( 0x2 )</dt> </dl>                          | 要求內容的唯讀存取權。<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <dt>**TF \_ES \_ READWRITE**</dt> <dt> ( 0x6 )</dt> </dl>           | 要求內容的讀取/寫入存取權。<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <dt>**TF \_ES \_ ASYNC**</dt> <dt> ( 0x8 )</dt> </dl>                       | 編輯會話必須是非同步，否則要求將會失敗。 此值無法與 TF \_ es \_ ASYNCDONTCARE 或 tf \_ es \_ 同步值結合。<br/>                                                                                                                                                                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITfCoNtext：： RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





