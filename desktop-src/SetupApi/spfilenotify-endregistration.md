---
description: SPFILENOTIFY_ENDREGISTRATION 訊息-使用 RegisterDlls INF 指示詞自行註冊 Dll 時，SetupInstallFromInfSection 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: 'SPFILENOTIFY_ENDREGISTRATION 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec341c26f9f88390ff1b807e6e932b3b381cd57
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094506"
---
# <a name="spfilenotify_endregistration-message"></a>SPFILENOTIFY \_ ENDREGISTRATION 訊息

使用 **RegisterDlls** INF 指示詞來自行註冊 dll 時， [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。 若要在註冊或取消註冊檔案之後，將 **SPFILENOTIFY \_ ENDREGISTRATION** 通知傳送給回呼常式，請 \_ \_ 在 **SPINST** 的 *Flags* 參數中包含 SPINST REGISTERCALLBACKAWARE plus REGSVR SetupInstallFromInfSection。 若要傳送取消註冊的通知，請 \_ \_ 在 *Flags* 參數中包含 SPINST REGISTERCALLBACKAWARE plus SPINST UNREGSVR。

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)的 *MsgHandler* 參數所指定的回呼常式必須是 [PSP 檔案 \_ \_ 回呼](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)類型。 將 *coNtext* 參數設定為 **SetupInstallFromInfSection** 中指定的相同 *內容*。 將 *通知* 參數設定為 **SPFILENOTIFY \_ ENDREGISTRATION**。


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

SP 暫存器 [**\_ \_ 控制 \_ 狀態**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) 結構的指標，其中包含要註冊或取消註冊之檔案的相關資訊。 成員 **cbsize** 應該設定為結構的大小。 **檔案名** 應設定為所註冊之檔案的完整路徑。 **Win32Error** 應該設定為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) ，指出擴充的錯誤碼。 **FailureCode** 應該設定為其中一個表示註冊結果的有效失敗代碼。 如需有效的失敗碼，請參閱 [**SP \_ 註冊 \_ 控制 \_ 狀態**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa)。

</dd> <dt>

*Param2* 
</dt> <dd>

如果正在註冊檔案， *Param2* 應該設定為非零值的指標。 如果檔案正在取消註冊， *Param2* 應該設定為零的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

收到通知之後，回呼函數可能會傳回下列其中一個值。



| 傳回碼                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl> | 停止處理 INF 區段。<br/>     |
| <dl> <dt>**FILEOP \_ DOIT R**</dt> </dl>  | 繼續處理 INF 區段。<br/> |
| <dl> <dt>**FILE \_ SKIP**</dt> </dl>    | 繼續處理 INF 區段<br/>  |



 

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

[**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)
</dt> </dl>

 

