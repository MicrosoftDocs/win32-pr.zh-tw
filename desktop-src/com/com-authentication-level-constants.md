---
title: '驗證層級常數 (Rpcdce) '
description: 這些值會指定驗證層級，指出提供來協助保護資料完整性的驗證數量。 每個層級都包含先前層級所提供的保護。
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509428"
---
# <a name="authentication-level-constants"></a>驗證層級常數

這些值會指定驗證層級，指出提供來協助保護資料完整性的驗證數量。 每個層級都包含先前層級所提供的保護。



| 常數/值                                                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 層級 \_ 預設值**</dt> <dt>0</dt> </dl>                    | 告訴 DCOM 使用其一般安全性整體協商演算法來選擇驗證等級。 如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。 <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 層級 \_ 無**</dt> <dt>1</dt> </dl>                             | 不執行任何驗證。<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_C \_ 驗證 \_ LEVEL \_ CONNECT**</dt> <dt>2</dt> </dl>                    | 只有當用戶端建立與伺服器之間的關聯性時，才會驗證用戶端的認證。 資料包傳輸一律改用 RPC \_ 驗證 \_ 層級 \_ PKT。 <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 層級 \_ 呼叫**</dt> <dt>3</dt> </dl>                             | 當伺服器收到要求時，只會在每個遠端程序呼叫的開頭進行驗證。 資料包傳輸會改為使用 RPC \_ C \_ 驗證 \_ 層級 \_ PKT。<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_C \_ 驗證 \_ LEVEL \_ PKT**</dt> <dt>4</dt> </dl>                                | 驗證收到的所有資料都是來自預期的用戶端。<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_C \_ 驗證 \_ LEVEL \_ PKT \_ 完整性**</dt> <dt>5</dt> </dl> | 驗證並確認在用戶端與伺服器之間傳送的資料都沒有修改。<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**</dt> <dt>6</dt> </dl>       | 驗證所有先前的層級，並加密每個遠端程序呼叫的引數值。<br/>                                                                                                    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce。h</dt> </dl> |



 

 





