---
title: 'TB_SAVERESTORE 訊息 (Commctrl .h) '
description: 傳送此訊息以起始儲存或還原工具列狀態。
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843059"
---
# <a name="tb_saverestore-message"></a>TB \_ SAVERESTORE 訊息

傳送此訊息以起始儲存或還原工具列狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

儲存或還原旗標。 如果此參數為 **TRUE**，則會儲存資訊。 如果為 **FALSE**，則會還原資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)結構的指標，指定工具列狀態資訊的登錄機碼、子機碼和值名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

針對4.72 版和更早的版本，若要使用這個訊息儲存或還原工具列，工具列控制項的父視窗必須執行 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) 通知程式碼的處理常式。 工具列會發出此通知，以在每個按鈕還原時取得其相關資訊。

5.80 版包含新的儲存/還原選項。 在程式開始時，當每個按鈕儲存或還原時，您的應用程式將會收到 [TBN \_ 儲存](tbn-save.md) 或 [TBN \_ 還原](tbn-restore.md) 通知。 若要使用此選項，您必須執行通知處理常式，為 Shell 提供成功儲存或還原工具列狀態所需的點陣圖和狀態資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_SAVERESTOREW** (Unicode) 和 **TB \_ SAVERESTOREA** (ANSI) <br/>             |



 

 





