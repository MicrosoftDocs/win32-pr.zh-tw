---
title: '管理員傳回值 (Msctf .h) '
description: 文字服務架構會從0xHHHH0200 到0xHHHH0507 的範圍內產生傳回值。 下表提供管理員以字母順序排列的值。
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea9c813f9ba71371f45e2475f73af4f3016e17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509139"
---
# <a name="manager-return-values"></a>管理員傳回值

文字服務架構會從 0x *hhhh hhhh* 0200 到 0x *hhhh hhhh* 0507 的範圍產生傳回值。 下表提供管理員以字母順序排列的值。

> [!Note]  
> 提供的描述不是特定的;傳回值的意義會根據傳回值的方法而不同。

 



| 傳回碼/值                                                                                                                                                                                                                                                   | Description                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <dt>**TF \_E \_ 已經 \_ 存在**</dt> <dt>0x80040506</dt> </dl>                   | 已註冊保留的金鑰。<br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <dt>**TF \_E \_ 組合已 \_ 拒絕**</dt> <dt>0x80040508</dt> </dl> | 內容擁有者拒絕撰寫。<br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <dt>**TF \_E \_ 中斷**</dt>連線 <dt>0x80040504</dt> </dl>                          | 內容物件不在檔堆疊上。<br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <dt>**TF \_E \_ EMPTYCONTEXT**</dt> <dt>0x80040509</dt> </dl>                          | 內容是空的。<br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <dt>**TF \_E \_ FORMAT**</dt> <dt>0x8004020a</dt> </dl>                                            | 內容擁有者無法處理 pDataObject 參數所提供之類型的物件。<br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <dt>**TF \_E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl>                          | 螢幕座標無效。<br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <dt>**TF \_E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>                                | 字元位置無效。<br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <dt>**TF \_E \_ INVALIDVIEW**</dt> <dt>0x80040505</dt> </dl>                             | 內容視圖無效。<br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <dt>**TF \_E \_ 鎖定**</dt>的 <dt>0x80040500</dt> </dl>                                            | 已經鎖定內容。<br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <dt>**TF \_E \_ NOINTERFACE**</dt> <dt>0x80040204</dt> </dl>                             | 物件不支援要求的介面。<br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <dt>**TF \_E \_ NOLAYOUT**</dt> <dt>0x80040206</dt> </dl>                                      | 尚未計算文字版面配置。<br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <dt>**TF \_E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                                            | 呼叫端沒有所需的檔案類型。<br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <dt>**TF \_E \_ NOOBJECT**</dt> <dt>0x80040202</dt> </dl>                                      | 指定的位置不存在任何内嵌物件。<br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <dt>**TF \_E \_ NOPROVIDER**</dt> <dt>0x80040503</dt> </dl>                                | 指定的函式沒有函數提供者存在。<br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <dt>**TF \_E \_ NOSELECTION**</dt> <dt>0x80040205</dt> </dl>                             | 內容中不存在任何選取範圍。<br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <dt>**TF \_E \_ NOSERVICE**</dt> <dt>0x80040203</dt> </dl>                                   | 指定的服務不存在或無法建立。<br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <dt>**TF \_E \_ NOTOWNEDRANGE**</dt> <dt>0x80040502</dt> </dl>                       | TSF 管理員不會擁有此範圍。<br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <dt>**TF \_E \_ 範圍 \_ 未 \_ 涵蓋**</dt> <dt>0x80040507</dt> </dl>         | 範圍不在現用組合內。<br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <dt>**TF \_E \_ READONLY**</dt> <dt>0x80040209</dt> </dl>                                      | 編輯內容是唯讀的。<br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <dt>**TF \_E \_ STACKFULL**</dt> <dt>0x80040501</dt> </dl>                                   | 內容堆疊已滿。<br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <dt>**TF \_E \_ 同步**</dt> <dt>0x80040208</dt> </dl>                             | 無法取得同步的唯讀鎖定。<br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <dt>**TF \_S \_ ASYNC**</dt> <dt>0x00040300</dt> </dl>                                               | 資料將會以非同步方式取得。<br/>                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



 

 





