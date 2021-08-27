---
title: EmailAction。 Body 屬性
description: 針對腳本，取得或設定包含電子郵件訊息的電子郵件內文。
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- 主體屬性工作排程器
- Body 屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，主體屬性
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57daf8d16da9f77a88d91a23cfaea88d1c3e27adb09a0d502b447b5987fce2ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100378"
---
# <a name="emailactionbody-property"></a>EmailAction。 Body 屬性

\[不再支援此物件。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]

針對腳本，取得或設定包含電子郵件訊息的電子郵件內文。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>屬性值

包含電子郵件訊息的電子郵件內文。

## <a name="remarks"></a>備註

設定這個屬性值時，值可以是從資源 .dll 檔抓取的文字。 特製化的字串會用來參考資源檔中的文字。 字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ Dll \] 是包含資源的 .dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。 例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                    |
| 伺服器支援結束<br/>    | Windows Server 2008 R2<br/>                                                       |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

