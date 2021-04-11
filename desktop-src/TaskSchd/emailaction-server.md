---
title: EmailAction。伺服器屬性
description: 針對腳本，取得或設定用來傳送電子郵件的 SMTP 伺服器名稱。
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- 伺服器屬性工作排程器
- 伺服器屬性工作排程器，EmailAction 物件
- EmailAction 物件工作排程器，伺服器屬性
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317284"
---
# <a name="emailactionserver-property"></a>EmailAction。伺服器屬性

\[不再支援此物件。 請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]

針對腳本，取得或設定用來傳送電子郵件的 SMTP 伺服器名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>屬性值

您用來傳送電子郵件的伺服器名稱。

## <a name="remarks"></a>備註

請確認傳送電子郵件的 SMTP 伺服器已正確設定。 電子郵件是使用適用于 Windows SMTP 伺服器的 NTLM 驗證來傳送，這表示用於執行工作的安全性認證也必須具有 SMTP 伺服器的許可權，才能傳送電子郵件訊息。 如果 SMTP 伺服器是非 Windows 伺服器，則會在伺服器允許匿名存取時傳送電子郵件。 如需設定 SMTP 伺服器的詳細資訊，請參閱 [Smtp 伺服器設定](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)，如需管理 smtp 伺服器設定的詳細資訊，請參閱 [smtp 管理](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
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

 

