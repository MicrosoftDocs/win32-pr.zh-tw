---
description: 通訊協定處理常式所傳回的錯誤訊息：
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: '搜尋通訊協定處理常式錯誤訊息 (Searchapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4473e3e235641e5b4bb5d86313b4154cd00ec029fe96d42d8964dab51f33780f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969727"
---
# <a name="search-protocol-handler-error-messages"></a>搜尋通訊協定處理常式錯誤訊息

通訊協定處理常式所傳回的錯誤訊息：



| 常數/值                                                                                                                                                                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_\_ \_ 拒絕拒絕存取**</dt> <dt>0x80041205L</dt> </dl>             | 存取遭到拒絕。 如果發生這種情況，則會從收集程式的 URL 佇列中刪除該檔案。<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_E \_ ACL \_ 為 \_ READ \_ NONE**</dt> <dt>0x80041211L</dt> </dl>  | 專案將不會編制索引。 它的 ACL 不允許任何人讀取該專案。<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_E \_ ACL \_ 太 \_ 大**</dt> <dt>0x80041212L</dt> </dl>                  | ACL 超過 64 KB。 搜尋不會為專案編制索引。<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_E \_ 錯誤的 \_ 要求**</dt> <dt>0x80041208L</dt> </dl>                   | 因為 URL 中有錯誤，所以要求無效。<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_E \_ 通訊 \_ 錯誤**</dt> <dt>0x80041200L</dt> </dl>                      | 表示通訊或伺服器錯誤。 如果特定伺服器有太多錯誤，收集程式會將伺服器標示為無法使用。<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_E \_ 未重新 \_ 導向**</dt> <dt>0x80041207L</dt> </dl>          | 重新導向的 URL 不存在。<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_E \_ OBJ \_ \_ 找不到**</dt> <dt>0x80041201L</dt> </dl>            | 找不到物件。 指出如果在遞增編目期間找不到記錄，則收集程式應從佇列中刪除該檔。<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_E \_ 要求 \_ 錯誤**</dt> <dt>0x80041202L</dt> </dl>             | 不支援使用的選項。<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_E \_ SERVER \_ 錯誤**</dt> <dt>0x80041206L</dt> </dl>                | 通訊或伺服器錯誤。 如果特定伺服器有太多錯誤，收集程式會將伺服器標示為無法使用。<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_\_不是 \_ 所有 \_ 元件**</dt> <dt>0x8004121BL</dt> </dl>            | 無法存取專案的部分。<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_S \_ 未 \_ 修改**</dt> <dt>0x00041203L</dt> </dl>                | 專案內容尚未變更。 如果此錯誤發生在增量編目期間，則收集程式會略過此專案，因為專案未變更。<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_S \_ 嘗試 \_**</dt>模擬 <dt>0x00041225L</dt> </dl> | 模擬使用者時應存取專案。 通訊協定處理常式必須執行 [**IUrlAccessor3：： GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) ，如此搜尋通訊協定主機才能抓取要用於模擬的 sid 清單，並且可以還原為使用 [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2)，在開啟專案時模擬其中一個允許的使用者。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP SP2，僅 Windows Vista \[ 桌面應用程式\]<br/>                    |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>                                            |
| 標頭<br/>                   | <dl> <dt>Searchapi。h</dt> </dl> |



 

 




