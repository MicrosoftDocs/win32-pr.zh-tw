---
title: 'EM_SETCUEBANNER 訊息 (Commctrl .h) '
description: 設定 [編輯] 控制項所顯示的文字提示或提示，以提示使用者輸入資訊。
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466548"
---
# <a name="em_setcuebanner-message"></a>EM \_ SETCUEBANNER 訊息

設定 [編輯] 控制項所顯示的文字提示或提示，以提示使用者輸入資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

如果在編輯控制項有焦點時，提示橫幅應該會顯示，則 **為 TRUE** 。否則 **為 FALSE**。 **FALSE** 是當使用者按一下控制項時，提示橫幅消失的預設行為。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

Unicode 字串的指標，其中包含要顯示為文字提示的文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則會傳回 **TRUE**。 否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

用來開始搜尋的編輯控制項可能會以灰色文字顯示為文字提示的「輸入搜尋」。 當使用者按一下文字時，文字會消失，使用者可以輸入。

您無法在多行編輯控制項或 rich edit 控制項上設定提示橫幅。

> [!Note]  
> 若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯 \_ SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





