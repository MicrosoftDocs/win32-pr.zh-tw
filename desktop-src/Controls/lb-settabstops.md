---
title: 'LB_SETTABSTOPS 訊息 (Winuser .h) '
description: 設定清單方塊中的定位停駐點位置。
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- LB_SETTABSTOPS message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844104"
---
# <a name="lb_settabstops-message"></a>LB \_ SETTABSTOPS 訊息

設定清單方塊中的定位停駐點位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定制表位的數目。

</dd> <dt>

*lParam* 
</dt> <dd>

包含索引標籤之整數陣列的第一個成員指標。 整數表示在清單方塊中選取之字型的平均字元寬度的季數。 例如，4的 tab 鍵會放在1.0 個字元的單位，而索引標籤停止的位置則是1.5 個平均字元單位。 但是，如果清單方塊是對話方塊的一部分，則整數會在對話方塊範本單位中。 定位停駐點必須以遞增順序排序;不允許反向索引標籤。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果設定了所有指定的索引標籤，則傳回值為 **TRUE**;否則為 **FALSE**。

## <a name="remarks"></a>備註

若要回應 **LB \_ SETTABSTOPS** 訊息，必須以 [**磅 \_ USETABSTOPS**](list-box-styles.md) 樣式建立清單方塊。

如果 *wParam* 為0，而 *lParam* 為 **Null**，則預設的 tab 鍵會停止為兩個對話方塊範本單位。 如果 *wParam* 是1，則清單方塊會以 *lParam* 所指定的距離分隔 tab 鍵。

如果 *lParam* 指向一個以上的值，將會針對 *lParam* 中的每個值設定制表位，最多可達 *wParam* 所指定的數位。

*LParam* 所指定的值位於對話方塊範本單位中，也就是對話方塊範本中使用的裝置獨立單位。 若要將度量從對話方塊範本單位轉換為螢幕單位 (圖元) ，請使用 [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) 函數。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *LParam* 所指向的緩衝區必須位於可寫入的記憶體中，即使訊息並未修改陣列也是一樣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

