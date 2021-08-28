---
title: 'CCM_SETVERSION 訊息 (Commctrl .h) '
description: 此訊息是用來通知控制項您預期會有與特定版本相關聯的行為。
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9453b99ff9cd23675b3b5d79593071e4ebb3fbb65d06a78d0fe8094154b2486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320098"
---
# <a name="ccm_setversion-message"></a>CCM \_ SETVERSION 訊息

此訊息是用來通知控制項您預期會有與特定版本相關聯的行為。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

版本號碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前 **CCM \_ SETVERSION** 訊息中指定的版本。 如果 *wParam* 設定為大於目前 DLL 版本的值，則會傳回-1。

## <a name="remarks"></a>備註

在少數情況下，控制項的行為可能會不同，視版本而定。 這主要適用于在較新版本中修正的 bug。 **CCM \_ SETVERSION** 訊息可讓您通知控制項預期的行為。 您可以藉由傳送 [**CCM \_ GETVERSION**](ccm-getversion.md) 訊息來判斷所指定的版本。 如需如何使用此訊息的範例，請參閱 [使用 List-View 和 Tree-View 控制項的自訂繪製](custom-draw.md)。

如果您已安裝 ComCtl32.dll 版本6，不論您在 *wParam* 中設定的值為何， **CCM \_ SETVERSION** 訊息都會傳回第6版。

> [!Note]  
> 此訊息只會設定其傳送目標控制項的版本號碼。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





