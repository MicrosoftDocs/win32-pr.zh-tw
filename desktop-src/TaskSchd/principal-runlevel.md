---
title: Principal. RunLevel 屬性
description: 針對腳本，取得或設定用來指定執行與主體相關聯之工作所需之許可權等級的識別碼。
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- RunLevel 屬性工作排程器
- RunLevel 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，RunLevel 屬性
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2bc9552ac8650bb2cf9ca40944a480683f2ef6dc6cccecfc5ed34eb544ca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126128"
---
# <a name="principalrunlevel-property"></a>Principal. RunLevel 屬性

針對腳本，取得或設定用來指定執行與主體相關聯之工作所需之許可權等級的識別碼。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>屬性值

用來指定執行與主體相關聯之工作所需之許可權層級的識別碼。



| 值                                                                                                                                                                                                                                         | 意義                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**工作 \_RUNLEVEL \_ LUA**</dt> <dt>0</dt> </dl>             | 工作會以最少的許可權執行， (LUA) 。<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**工作 \_RUNLEVEL \_ 最高**</dt> <dt>1</dt> </dl> | 工作會以最高的許可權執行。<br/>     |



 

## <a name="remarks"></a>備註

如果工作是使用內建 \\ 系統管理員帳戶或本機系統或本地服務帳戶來註冊的，則會忽略 **RunLevel** 屬性。 如果已關閉使用者帳戶控制 (UAC) ，也會忽略屬性值。

如果工作是使用工作安全性內容的 Administrators 群組來註冊的，則您也必須將 [ [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ] 屬性設定為 [ **task \_ RunLevel \_** ] （如果您想要執行此工作）。 如需詳細資訊，請參閱工作 [的安全性](security-contexts-for-running-tasks.md)內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主要**](principal.md)
</dt> </dl>

 

 





