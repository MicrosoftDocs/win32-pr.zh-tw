---
title: 'CB_GETCUEBANNER 訊息 (Winuser .h) '
description: 取得在下拉式方塊的編輯控制項中顯示的提示橫幅文字。 明確地傳送此訊息，或使用 ComboBox \_ GetCueBannerText 宏。
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843823"
---
# <a name="cb_getcuebanner-message"></a>CB \_ GETCUEBANNER 訊息

取得在下拉式方塊的編輯控制項中顯示的提示橫幅文字。 明確地傳送此訊息，或使用 [**ComboBox \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

Unicode 字串緩衝區的指標，此緩衝區會接收提示橫幅文字。 呼叫應用程式負責配置緩衝區的記憶體。 緩衝區大小必須等於 **WCHARs** 中的提示橫幅字串長度，再加上1表示終止的 **Null** **WCHAR**。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

*LpcwText* 在 **WCHARs** 中所指向的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回1，否則會傳回錯誤值。

如果沒有要取得的提示橫幅文字，則傳回值為0。 如果呼叫的應用程式無法配置緩衝區，或在傳送此訊息之前設定 *lParam* ，則可能會產生未定義的行為，而且傳回值可能不可靠。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[下拉式列示方塊功能](combo-box-features.md)
</dt> </dl>

 

 





