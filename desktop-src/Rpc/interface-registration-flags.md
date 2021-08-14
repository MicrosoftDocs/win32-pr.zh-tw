---
title: '介面註冊旗標 (Rpcdce .h) '
description: RpcServerRegisterIf2 和 RpcServerRegisterIfEx 函數的 Flags 參數中會使用下列常數。
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33111bc7dc1acdf5ec12ba81b91b9ec37d7b9994c1af3821c0997562f49e81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928894"
---
# <a name="interface-registration-flags"></a>介面註冊旗標

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)和 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)函數的 *Flags* 參數中會使用下列常數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>0</strong></dt> </dl></td>
<td style="text-align: left;">標準介面語義。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">註冊這個介面旗標時，RPC 執行時間會叫用所有呼叫的已註冊安全性回呼，而不論身分識別、通訊協定順序或用戶端的驗證層級為何。<br/>
<blockquote>
[!Note]<br />
此旗標從 Windows XP SP2 和 Windows Server 2003 SP1 開始提供。 如果未設定此旗標，RPC 會在所有未經驗證的呼叫到達安全性回呼之前自動進行篩選。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">註冊這個介面旗標時，RPC 執行時間會拒絕遠端用戶端所發出的呼叫。 使用 ncadg_ * 和 ncacn_ * 通訊協定序列的所有本機呼叫也會被拒絕，但 ncacn_np 除外。 RPC 只在呼叫不是來自 SRV 時，才允許 ncacn_NP 呼叫。 一律會處理來自 ncalrpc 的呼叫。<br/>
<blockquote>
[!Note]<br />
此旗標從 Windows XP SP2 和 Windows Server 2003 SP1 開始提供。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">這是 <strong>自動接聽</strong> 介面。 當第一個 autolisten 介面註冊之後，執行時間就會開始接聽呼叫，並在上一次 autolisten 介面未註冊時停止接聽。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <dt><strong>RPC_IF_OLE</strong></dt> </dl></td>
<td style="text-align: left;">保留給 OLE。 請勿使用此旗標。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </dl></td>
<td style="text-align: left;">目前尚未實作。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">限制使用高於 RPC_C_AUTHN_LEVEL_NONE 的授權等級之用戶端的連接。 指定這個旗標可讓用戶端在 <strong>Null</strong> 會話上進行。 在 Windows XP 和 Windows Server 2003 上，不允許這類用戶端。 RPC_IF_ALLOW_SECURE_ONLY 測試失敗的用戶端會收到 RPC_S_ACCESS_DENIED 錯誤。 使用 RPC_IF_ALLOW_SECURE_ONLY 旗標並不代表或保證呼叫使用者的部分具有高階許可權。 RPC 只會檢查使用者是否擁有有效的認證;呼叫的使用者可能使用 guest 帳戶或其他低許可權帳戶。 使用 RPC_IF_ALLOW_SECURE_ONLY 時，請勿採用高許可權。<br/> <strong>Windows NT 4.0 和 Windows Me/98/95：</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">停用安全性回呼快取，針對指定介面上的每個 RPC 呼叫強制執行安全性回呼。<br/>
<blockquote>
[!Note]<br />
此旗標從 Windows XP SP2 和 Windows Server 2003 SP1 開始提供。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce。h</dt> </dl> |



 

 





