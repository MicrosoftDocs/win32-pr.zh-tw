---
title: RegisteredTask. RunEx 方法
description: 針對腳本，會使用指定的旗標和會話識別碼立即執行已註冊的工作。
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- RunEx 方法工作排程器
- RunEx 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，RunEx 方法
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecea66d57bf473b5000e84c707e652f1c49431a840da5cc50e43f9e091c3eefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943390"
---
# <a name="registeredtaskrunex-method"></a>RegisteredTask. RunEx 方法

針對腳本，會使用指定的旗標和會話識別碼立即執行已註冊的工作。

## <a name="syntax"></a>語法


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*params* \[在\]
</dt> <dd>

用來當做工作動作中之值的參數。 若不指定工作動作的任何參數值，請將此參數設定為 **Nothing**。 否則，可以指定單一字串值或字串值的陣列。

您指定的字串值會與名稱配對，並以名稱/值組的形式儲存。 如果您指定單一字串值，則 Arg0 將會是指派給值的名稱。 此值可以在工作動作中使用，其中 $ (Arg0) 變數會在動作屬性中使用。

如果您傳入值（例如 "0"、"100" 和 "250"）做為字串值的陣列，則 "0" 將取代 $ (Arg0) 變數，"100" 將取代 $ (Arg1) 變數，而 "250" 將取代動作屬性中使用的 $ (Arg2) 變數。

最多可以指定32個字串值。

如需詳細資訊和可使用 $ (Arg0) ，$ (Arg1) ，...，$ (Arg32) 變數值的動作屬性清單，請參閱工作 [動作](task-actions.md)。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

工作 [ \_ 執行 \_ 旗標](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) 常數，定義工作的執行方式。

</dd> <dt>

*sessionID* \[在\]
</dt> <dd>

您要在其中啟動工作的終端機伺服器會話。

如果工作 \_ 執行 \_ 使用 \_ 會話 \_ 識別碼常數 (0x4) 不會傳遞至 *flags* 參數，則會忽略此參數中指定的值。 如果工作回合 \_ \_ 使用 \_ 會話 \_ 識別碼常數傳遞至 *flags* 參數，且 sessionID 值小於或等於0，則會傳回不正確引數錯誤。

如果工作回合 \_ \_ 使用 \_ 會話 \_ 識別碼常數傳遞至 *旗標* 參數，且 sessionID 值是大於0的有效會話識別碼，且如果沒有為 *使用者* 參數指定任何值，則工作排程器服務會嘗試以互動方式啟動工作，就像登入指定會話的使用者一樣。

如果工作回合 \_ \_ 使用 \_ 會話 \_ 識別碼常數傳遞至 *旗標* 參數，且 sessionID 值是大於0的有效會話識別碼，且使用者參數中指定了使用者，則工作排程器服務會嘗試以互動方式啟動工作，就像使用者參數中指定的使用者一樣。 

</dd> <dt>

*runningTask* \[擴展\]
</dt> <dd>

定義工作新實例的 [**RunningTask**](runningtask.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會傳回而不會發生錯誤，但是如果已註冊工作的 [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) 屬性設定為 false，則不會執行此工作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





