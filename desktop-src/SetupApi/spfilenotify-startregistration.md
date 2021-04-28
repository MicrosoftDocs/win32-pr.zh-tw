---
description: SPFILENOTIFY_STARTREGISTRATION 訊息-使用 RegisterDlls INF 指示詞自行註冊 Dll 時，SetupInstallFromInfSection 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: 'SPFILENOTIFY_STARTREGISTRATION 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e71a884d079515436f296faf515a83a985311e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094496"
---
# <a name="spfilenotify_startregistration-message"></a>SPFILENOTIFY \_ STARTREGISTRATION 訊息

使用 **RegisterDlls** INF 指示詞來自行註冊 dll 時， [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。 若要在註冊檔案之前將 **SPFILENOTIFY \_ STARTREGISTRATION** 通知傳送給回呼常式一次，請 \_ \_ 在 **SPINST** 的 *旗標* 參數中包含 SPINST REGISTERCALLBACKAWARE plus REGSVR SetupInstallFromInfSection。 若要傳送取消註冊的通知，請 \_ \_ 在 *Flags* 參數中包含 SPINST REGISTERCALLBACKAWARE plus SPINST UNREGSVR。

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)的 *MsgHandler* 參數所指定的回呼常式必須是 [PSP 檔案 \_ \_ 回呼](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)類型。 將 *coNtext* 參數設定為 **SetupInstallFromInfSection** 中指定的相同 *內容*。 將 *通知* 參數設定為 **SPFILENOTIFY \_ STARTREGISTRATION**。


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

SP 暫存器 [**\_ \_ 控制 \_ 狀態**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) 結構的指標，其中包含要註冊或取消註冊之檔案的相關資訊。 成員 **cbsize** 應該設定為結構的大小。 **FileName** 成員應設定為所註冊之檔案的完整路徑。 **Win32Error** 不會使用，且應該設定為無 \_ 錯誤。 **FailureCode** 不會使用，且應設定為 SPREG \_ SUCCESS。

</dd> <dt>

*Param2* 
</dt> <dd>

如果正在註冊檔案， *Param2* 應該設定為非零值的指標。 如果檔案正在取消註冊， *Param2* 應該設定為零的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

收到通知之後，回呼函數可能會傳回下列其中一個值。



| 傳回碼                                                                                  | Description                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl> | 請勿註冊或取消註冊檔案，並停止處理 INF 區段。<br/>             |
| <dl> <dt>**FILEOP \_ DOIT R**</dt> </dl>  | 註冊或取消註冊檔案，並繼續處理 INF 區段。<br/>                |
| <dl> <dt>**FILE \_ SKIP**</dt> </dl>    | 略過註冊或取消註冊檔案，但繼續處理 INF 區段<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Setupapi.log。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[概觀](overview.md)
</dt> <dt>

[通知](notifications.md)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)
</dt> </dl>

 

