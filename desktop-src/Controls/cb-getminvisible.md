---
title: 'CB_GETMINVISIBLE 訊息 (Commctrl .h) '
description: 取得下拉式方塊下拉式清單中可見專案的最小數目。
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- CB_GETMINVISIBLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8860b0c68d00d24fa5a5f824f6091a14e3f4d82010f5ee80fd195d17d4ea5096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006745"
---
# <a name="cb_getminvisible-message"></a>CB \_ GETMINVISIBLE 訊息

取得下拉式方塊下拉式清單中可見專案的最小數目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是可見專案的最小數目。

## <a name="remarks"></a>備註

當下拉式清單中的專案數目大於最小值時，下拉式方塊就會使用捲軸。

如果下拉式方塊控制項的樣式為 [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md)，則會忽略此訊息。

若要使用 **CB \_ GETMINVISIBLE**，應用程式必須在資訊清單中指定 comctl32.dll 第6版。 如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ SETMINVISIBLE**](cb-setminvisible.md)
</dt> <dt>

[**ComboBox \_ GetMinVisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





