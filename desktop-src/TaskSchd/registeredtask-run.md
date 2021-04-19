---
title: RegisteredTask 方法
description: 針對腳本，會立即執行已註冊的工作。
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Run 方法工作排程器
- Run 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，Run 方法
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966137"
---
# <a name="registeredtaskrun-method"></a>RegisteredTask 方法

針對腳本，會立即執行已註冊的工作。

## <a name="syntax"></a>語法


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
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

*ppRunningTask* \[擴展\]
</dt> <dd>

定義工作新實例的 [**RunningTask**](runningtask.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**RegisteredTask** 函式相當於 [**RegisteredTask. RunEx**](registeredtask-runex.md)函式，其 flags 參數等於0，而且沒有針對使用者參數指定任何專案。

這個方法會傳回而不會發生錯誤，但是如果已註冊工作的 [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) 屬性設定為 false，則不會執行此工作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





