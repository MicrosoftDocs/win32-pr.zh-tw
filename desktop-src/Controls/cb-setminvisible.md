---
title: 'CB_SETMINVISIBLE 訊息 (Commctrl .h) '
description: 應用程式會傳送 CB \_ SETMINVISIBLE 訊息，在下拉式方塊的下拉式清單中設定可見專案的最小數目。
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9790c43141ef836c1dec86304f260b0490854b593b7005b594d2a718332296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063318"
---
# <a name="cb_setminvisible-message"></a>CB \_ SETMINVISIBLE 訊息

應用程式會傳送 **CB \_ SETMINVISIBLE** 訊息，在下拉式方塊的下拉式清單中設定可見專案的最小數目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定可見專案的最小數目。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為 **TRUE**。 否則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

當下拉式清單中的專案數目大於最小值時，下拉式方塊就會使用捲軸。 根據預設，30是可見專案的最小數目。

如果下拉式方塊控制項的樣式為 [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md)，則會忽略此訊息。

若要使用 **CB \_ SETMINVISIBLE**，應用程式必須在資訊清單中指定 comctl32.dll 第6版。 如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

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

[**CB \_ GETMINVISIBLE**](cb-getminvisible.md)
</dt> <dt>

[**ComboBox \_ SetMinVisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





