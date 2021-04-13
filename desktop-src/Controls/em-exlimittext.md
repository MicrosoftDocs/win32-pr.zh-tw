---
title: 'EM_EXLIMITTEXT 訊息 (Richedit .h) '
description: 將使用者可以輸入或貼上的文字數量上限設定為 rich edit 控制項。
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465896"
---
# <a name="em_exlimittext-message"></a>EM \_ EXLIMITTEXT 訊息

將使用者可以輸入或貼上的文字數量上限設定為 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

指定可以輸入的最大文字數量。 如果此參數為零，則會使用預設的最大值，也就是64K 個字元。 COM 物件會計算為單一字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

**Em \_ EXLIMITTEXT** 訊息所設定的文字限制不會限制您可以使用 [**Em \_ STREAMIN**](em-streamin.md)訊息將 *lParam* 設定為 SF text 來串流至 rich edit 控制項的文字數量 \_ 。 不過，它會限制您可以使用 **EM \_ STREAMIN** 訊息，將 *lParam* 設定為 SF rtf，以串流至 rich edit 控制項的文字數量 \_ 。

在呼叫 **EM \_ EXLIMITTEXT** 之前，使用者可以輸入的文字數量預設限制為32767個字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





