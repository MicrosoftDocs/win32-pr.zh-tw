---
description: 深入瞭解：分散式路由表傳回值
ms.assetid: 7f5f925a-b3ce-4829-b9a4-cfc68ec6b50e
title: '分散式路由表會傳回值 (的 Drt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82a80c6529a6488fb12ee36abedb9f460549d72eaa4956e198ffd2d118d11cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011566"
---
# <a name="distributed-routing-table-return-values"></a>分散式路由表傳回值

分散式路由技術通常會傳回下列錯誤碼：

> [!Note]  
> DRT 也會傳回 [Winsock 錯誤碼](/windows/desktop/WinSock/windows-sockets-error-codes-2)。

 



| 常數/值                                                                                                                                                                                                                                                                                                  | 描述                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FACILITY_DRT"></span><span id="facility_drt"></span><dl> <dt>**設備 \_DRT**</dt> <dt>0x98</dt> </dl>                                                                                            |                                                                                                                                                                 |
| <span id="DRT_E_TIMEOUT"></span><span id="drt_e_timeout"></span><dl> <dt>**DRT \_E \_ TIMEOUT**</dt> <dt>0x1001</dt> </dl>                                                                                      | DRT 作業已超時。<br/>                                                                                                                     |
| <span id="DRT_E_INVALID_KEY_SIZE"></span><span id="drt_e_invalid_key_size"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 金鑰 \_ 大小**</dt> <dt>0x1002</dt> </dl>                                                         | 指定的金鑰不符合或超過允許的 DRT 金鑰大小。<br/>                                                                               |
| <span id="DRT_E_INVALID_CERT_CHAIN"></span><span id="drt_e_invalid_cert_chain"></span><dl> <dt>**DRT \_電子 \_ 無效 \_ \_**</dt>的憑證鏈 <dt>0x1004</dt> </dl>                                                   | 未附加任何憑證存放區，或憑證鏈中有錯誤。<br/>                                                                |
| <span id="DRT_E_INVALID_MESSAGE"></span><span id="drt_e_invalid_message"></span><dl> <dt>**DRT \_電子 \_ 不正確 \_ 訊息**</dt> <dt>0x1005</dt> </dl>                                                             | 訊息超過允許的字元限制或格式不正確。<br/>                                                                        |
| <span id="DRT_E_NO_MORE"></span><span id="drt_e_no_more"></span><dl> <dt>**DRT \_E \_ 否 \_**</dt> <dt>0x1006</dt> </dl>                                                                                     | 沒有其他可用的事件資料。<br/>                                                                                                               |
| <span id="DRT_E_INVALID_MAX_ADDRESSES"></span><span id="drt_e_invalid_max_addresses"></span><dl> <dt>**DRT \_電子 \_ 不正確 \_ 最大 \_ 位址**</dt> <dt>0x1007</dt> </dl>                                          | 沒有位址可供使用，或位址數目超過20。<br/>                                                                                    |
| <span id="DRT_E_SEARCH_IN_PROGRESS"></span><span id="drt_e_search_in_progress"></span><dl> <dt>**DRT \_電子 \_ 搜尋 \_ \_ 進行中**</dt> <dt>0x1008</dt> </dl>                                                   | 搜尋操作已在進行中。<br/>                                                                                                           |
| <span id="DRT_E_INVALID_KEY"></span><span id="drt_e_invalid_key"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 金鑰**</dt> <dt>0x1009</dt> </dl>                                                                         | 提供的金鑰與產生的金鑰不符。<br/>                                                                                                           |
| <span id="DRT_S_RETRY"></span><span id="drt_s_retry"></span><dl> <dt>**DRT \_S \_ 重試**</dt> <dt>0x1010</dt> </dl>                                                                                            | 作業無法完成，但在第二次嘗試時可能會成功。<br/>                                                                         |
| <span id="DRT_E_INVALID_MAX_ENDPOINTS"></span><span id="drt_e_invalid_max_endpoints"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 最大 \_ 端點**</dt> <dt>0x1011</dt> </dl>                                          | 端點數目超過允許的端點數目上限。<br/>                                                                                           |
| <span id="DRT_E_INVALID_SEARCH_RANGE"></span><span id="drt_e_invalid_search_range"></span><dl> <dt>**DRT \_電子 \_ \_ 搜尋 \_ 範圍**</dt> <dt>0x1012</dt>無效 </dl>                                             | 最小和最大索引鍵值相等，但目標不同。<br/>                                                                                           |
| <span id="DRT_E_INVALID_PORT"></span><span id="drt_e_invalid_port"></span><dl> <dt>**DRT \_E \_ \_ 埠**</dt> <dt>0x2000</dt>無效 </dl>                                                                      | 指定的埠值為 **Null**。<br/>                                                                                                                |
| <span id="DRT_E_INVALID_TRANSPORT_PROVIDER"></span><span id="drt_e_invalid_transport_provider"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 傳輸 \_ 提供者**</dt> <dt>0x2001</dt> </dl>                           | 指定的傳輸提供者無效。<br/>                                                                                                         |
| <span id="DRT_E_INVALID_SECURITY_PROVIDER"></span><span id="drt_e_invalid_security_provider"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 安全性 \_ 提供者**</dt> <dt>0x2002</dt> </dl>                              | 指定的安全性提供者無效。<br/>                                                                                                          |
| <span id="DRT_E_STILL_IN_USE"></span><span id="drt_e_still_in_use"></span><dl> <dt>**DRT \_E \_ 仍 \_ 在 \_ 使用中**</dt> <dt>0x2003</dt> </dl>                                                                     | 目前的 DRT 基礎結構忙碌中，無法完成此作業。<br/>                                                                          |
| <span id="DRT_E_INVALID_BOOTSTRAP_PROVIDER"></span><span id="drt_e_invalid_bootstrap_provider"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 啟動載入 \_ 器提供者**</dt> <dt>0x2004</dt> </dl>                           | 指定的啟動載入器提供者無效。<br/>                                                                                                         |
| <span id="DRT_E_INVALID_ADDRESS"></span><span id="drt_e_invalid_address"></span><dl> <dt>**DRT \_電子 \_ 不正確 \_ 位址**</dt> <dt>0x2005</dt> </dl>                                                             | 提供的位址不是接受和完整格式，或為 **Null**。<br/>                                                                     |
| <span id="DRT_E_INVALID_SCOPE"></span><span id="drt_e_invalid_scope"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 範圍**</dt> <dt>0x2006</dt> </dl>                                                                   | 指定的範圍不是在 [**DRT \_ 範圍**](/windows/desktop/api/drt/ne-drt-drt_scope)中定義的其中一個值。<br/>                                                             |
| <span id="DRT_E_TRANSPORT_SHUTTING_DOWN"></span><span id="drt_e_transport_shutting_down"></span><dl> <dt>**DRT \_E \_ 傳輸 \_ 關閉 \_**</dt> <dt>0x2007</dt> </dl>                                    | 指定的傳輸正在關閉中。<br/>                                                                                          |
| <span id="DRT_E_NO_ADDRESSES_AVAILABLE"></span><span id="drt_e_no_addresses_available"></span><dl> <dt>**DRT \_E \_ 無 \_ \_ 可用位址**</dt> <dt>0x2008</dt> </dl>                                       | 目前沒有遠端節點存在於 DRT 中。<br/>                                                                                              |
| <span id="DRT_E_DUPLICATE_KEY"></span><span id="drt_e_duplicate_key"></span><dl> <dt>**DRT \_E \_ 重複 \_**</dt>的索引鍵 <dt>0x2009</dt> </dl>                                                                   | 此金鑰已存在於 DRT 基礎結構中。<br/>                                                                                               |
| <span id="DRT_E_TRANSPORTPROVIDER_IN_USE"></span><span id="drt_e_transportprovider_in_use"></span><dl> <dt>**DRT \_\_ \_ \_ 使用中的電子 TRANSPORTPROVIDER**</dt> <dt>0x200a</dt> </dl>                                 | 指定的傳輸提供者已在使用中。<br/>                                                                                                  |
| <span id="DRT_E_TRANSPORTPROVIDER_NOT_ATTACHED"></span><span id="drt_e_transportprovider_not_attached"></span><dl> <dt>**DRT \_E \_ TRANSPORTPROVIDER \_ 未 \_ 附加**</dt> <dt>0x200b</dt> </dl>               | 未附加傳輸提供者。<br/>                                                                                                              |
| <span id="DRT_E_SECURITYPROVIDER_IN_USE"></span><span id="drt_e_securityprovider_in_use"></span><dl> <dt>**DRT \_\_ \_ \_ 使用中的電子 SECURITYPROVIDER**</dt> <dt>0x200c</dt> </dl>                                    | 指定的安全性提供者已在使用中。<br/>                                                                                                   |
| <span id="DRT_E_SECURITYPROVIDER_NOT_ATTACHED"></span><span id="drt_e_securityprovider_not_attached"></span><dl> <dt>**DRT \_E \_ SECURITYPROVIDER \_ 未 \_ 附加**</dt> <dt>0x200d</dt> </dl>                  | 未附加安全性提供者。<br/>                                                                                                               |
| <span id="DRT_E_BOOTSTRAPPROVIDER_IN_USE"></span><span id="drt_e_bootstrapprovider_in_use"></span><dl> <dt>**DRT \_\_ \_ \_ 使用中的電子 BOOTSTRAPPROVIDER**</dt> <dt>0x200e</dt> </dl>                                 | 指定的安全性提供者已在使用中。<br/>                                                                                                   |
| <span id="DRT_E_BOOTSTRAPPROVIDER_NOT_ATTACHED"></span><span id="drt_e_bootstrapprovider_not_attached"></span><dl> <dt>**DRT \_E \_ BOOTSTRAPPROVIDER \_ 未 \_ 附加**</dt> <dt>0x200f</dt> </dl>               | 啟動載入器提供者未附加。<br/>                                                                                                              |
| <span id="DRT_E_TRANSPORT_ALREADY_BOUND"></span><span id="drt_e_transport_already_bound"></span><dl> <dt>**DRT \_E \_ 傳輸 \_ 已 \_**</dt>系結 <dt>0x2101</dt> </dl>                                    | 傳輸已系結。<br/>                                                                                                                      |
| <span id="DRT_E_TRANSPORT_NOT_BOUND"></span><span id="drt_e_transport_not_bound"></span><dl> <dt>**DRT \_E \_ 傳輸 \_ 未 \_**</dt>系結 <dt>0x2102</dt> </dl>                                                | 傳輸未系結。<br/>                                                                                                                          |
| <span id="DRT_E_TRANSPORT_UNEXPECTED"></span><span id="drt_e_transport_unexpected"></span><dl> <dt>**DRT \_E \_ 傳輸未 \_ 預期**</dt>的 <dt>0x2103</dt> </dl>                                              | 傳輸時發生未預期的錯誤。<br/>                                                                                                   |
| <span id="DRT_E_TRANSPORT_INVALID_ARGUMENT"></span><span id="drt_e_transport_invalid_argument"></span><dl> <dt>**DRT \_E \_ 傳輸 \_ 不正確 \_ 引數**</dt> <dt>0x2104</dt> </dl>                           | 傳遞給傳輸的引數無效。<br/>                                                                                                     |
| <span id="DRT_E_TRANSPORT_NO_DEST_ADDRESSES"></span><span id="drt_e_transport_no_dest_addresses"></span><dl> <dt>**DRT \_E \_ TRANSPORT \_ NO \_ DEST \_ 位址**</dt> <dt>0x2105</dt> </dl>                       | 目的地位址尚未提供給傳輸。<br/>                                                                                       |
| <span id="DRT_E_TRANSPORT_EXECUTING_CALLBACK"></span><span id="drt_e_transport_executing_callback"></span><dl> <dt>**DRT \_E \_ 傳輸 \_ 執行 \_ 回呼**</dt> <dt>0x2106</dt> </dl>                     | 傳輸目前正在執行回呼作業。<br/>                                                                                           |
| <span id="DRT_E_TRANSPORT_ALREADY_EXISTS_FOR_SCOPE"></span><span id="drt_e_transport_already_exists_for_scope"></span><dl> <dt>**DRT \_0x2107 \_ \_ \_ \_ \_ 範圍的 E 傳輸已存在**</dt> <dt></dt> </dl> | 此 DRT 範圍已經存在傳輸。<br/>                                                                                                       |
| <span id="DRT_E_INVALID_SETTINGS"></span><span id="drt_e_invalid_settings"></span><dl> <dt>**DRT \_電子 \_ 不正確 \_ 設定**</dt> <dt>0x2108</dt> </dl>                                                          | 在 [**DRT 設定**](/windows/desktop/api/drt/ns-drt-drt_settings) 結構中所包含的資料無效，或相關的參數值為 **Null**。 <br/>                         |
| <span id="DRT_E_INVALID_SEARCH_INFO"></span><span id="drt_e_invalid_search_info"></span><dl> <dt>**DRT \_電子 \_ \_ 搜尋 \_ 資訊**</dt> <dt>0x2109</dt>無效 </dl>                                                | 在 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info) 結構中所包含的資料無效，或相關的參數值為 **Null**。 <br/>                |
| <span id="DRT_E_FAULTED"></span><span id="drt_e_faulted"></span><dl> <dt>**DRT \_E \_**</dt>錯誤 <dt>0x210a</dt> </dl>                                                                                      | DRT 基礎結構發生錯誤。 您必須呼叫 [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) 函式，之後才可以重新開啟該的 DRT。<br/> |
| <span id="DRT_E_TRANSPORT_STILL_BOUND"></span><span id="drt_e_transport_still_bound"></span><dl> <dt>**DRT \_E \_ 傳輸 \_ 仍 \_**</dt>系結 <dt>0x210b</dt> </dl>                                          | 傳輸目前已系結。<br/>                                                                                                                    |
| <span id="DRT_E_INSUFFICIENT_BUFFER"></span><span id="drt_e_insufficient_buffer"></span><dl> <dt>**DRT \_E \_ \_ 緩衝區**</dt> <dt>0x210c</dt>不足 </dl>                                                 | 緩衝區的大小不足以進行作業。<br/>                                                                                            |
| <span id="DRT_E_INVALID_INSTANCE_PREFIX"></span><span id="drt_e_invalid_instance_prefix"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 實例 \_ 前置**</dt>詞 <dt>0x210d</dt> </dl>                                    | DRT 實例首碼無效。<br/>                                                                                                                  |
| <span id="DRT_E_INVALID_SECURITY_MODE"></span><span id="drt_e_invalid_security_mode"></span><dl> <dt>**DRT \_E \_ 不正確 \_ 安全性 \_ 模式**</dt> <dt>0x210e</dt> </dl>                                          | 指定的安全性模式不是在 [**DRT \_ 安全性 \_ 模式**](/windows/desktop/api/drt/ne-drt-drt_security_mode)中定義的其中一個值。<br/>                                    |
| <span id="DRT_E_CAPABILITY_MISMATCH"></span><span id="drt_e_capability_mismatch"></span><dl> <dt>**DRT \_E \_ 功能 \_ 不符**</dt> <dt>0x210f</dt> </dl>                                                 | 無法使用要求的安全性演算法。<br/>                                                                                                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 專業版 \[僅限桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                          |
| 標頭<br/>                   | <dl> <dt>Drt</dt> </dl> |



 

