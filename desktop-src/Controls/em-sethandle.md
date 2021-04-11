---
title: 'EM_SETHANDLE 訊息 (Winuser .h) '
description: 設定多行編輯控制項將使用的記憶體控制碼。
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105575"
---
# <a name="em_sethandle-message"></a>EM \_ SETHANDLE 訊息

設定多行編輯控制項將使用的記憶體控制碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

記憶體緩衝區的控制碼，編輯控制項會用來儲存目前顯示的文字，而非配置它自己的記憶體。 必要時，控制項會重新配置此記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

在應用程式設定新的記憶體控制碼之前，它應該傳送 [**EM \_ GETHANDLE**](em-gethandle.md) 訊息來取出目前記憶體緩衝區的控制碼，而且應該釋放該記憶體。

編輯控制項會在需要額外的文字空間時，自動重新配置指定的緩衝區，或移除足夠的文字以不再需要額外的空間。

傳送 **EM \_ SETHANDLE** 訊息會清除復原緩衝區 ([**em \_ CANUNDO**](em-canundo.md) 會傳回零) 和內部修改旗標 ([**EM \_ GETMODIFY**](em-getmodify.md) 會傳回零) 。 會重新繪製編輯控制項視窗。

**Rich Edit：** 不支援 **EM \_ SETHANDLE** 訊息。 Rich edit 控制項不會將文字儲存為簡單字元陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> </dl>

 

 





