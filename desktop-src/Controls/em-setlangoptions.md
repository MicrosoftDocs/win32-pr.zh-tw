---
title: 'EM_SETLANGOPTIONS 訊息 (Richedit .h) '
description: 在 rich edit 控制項中設定輸入方法編輯器 (IME) 和亞洲語言支援的選項。
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934274"
---
# <a name="em_setlangoptions-message"></a>EM \_ SETLANGOPTIONS 訊息

在 rich edit 控制項中設定輸入方法編輯器 (IME) 和亞洲語言支援的選項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

指定語言選項。 如需可能值的清單，請參閱 [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回值1。

## <a name="remarks"></a>備註

**EM \_ SETLANGOPTIONS** 訊息會控制下列各項：

-   自動字型系結。
-   自動切換鍵盤。
-   自動調整字型大小大小。
-   使用使用者介面預設字型，而不是檔預設字型。
-   在 IME 組合期間對用戶端的通知。
-   IME 如何中止組合模式。
-   拼寫檢查、自動校正和觸控鍵盤預測。

這則訊息會設定所有語言選項旗標的值。 若要變更旗標的子集，請傳送 [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md) 訊息以取得目前的選項旗標、變更您需要變更的旗標，然後傳送 **EM \_ SETLANGOPTIONS** 訊息與結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)
</dt> </dl>

 

 





