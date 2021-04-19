---
description: 當文字輸入面板開啟時通知視窗。
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: 'MICROSOFT_TIP_OPENING_MSG 訊息 (Peninputpanel .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987846"
---
# <a name="microsoft_tip_opening_msg-message"></a>MICROSOFT \_ 秘訣 \_ 開啟 \_ 訊息訊息

當文字輸入面板開啟時通知視窗。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

目前未使用，應該是 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

目前未使用，應該是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

處理此訊息之後，應用程式應該呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 。 如需其傳回值的詳細資訊，請參閱 **DefWindowProc** 。

## <a name="remarks"></a>備註

此通知可讓您知道何時會開啟輸入面板。 如果您想要在發生這種情況時執行動作，請處理訊息、在處理常式中執行作業，然後將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。

> [!Note]  
> 此訊息也會在文字輸入面板已顯示，且使用者從鍵盤切換至手寫外觀時傳送。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista<br/>                                                                   |
| 標頭<br/> | <dl> <dt>Peninputpanel。h</dt> </dl> |



 

