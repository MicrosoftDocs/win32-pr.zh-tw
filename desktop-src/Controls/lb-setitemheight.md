---
title: 'LB_SETITEMHEIGHT 訊息 (Winuser .h) '
description: 設定清單方塊中專案的高度（以圖元為單位）。 如果清單方塊具有磅 \_ OWNERDRAWVARIABLE 樣式，則此訊息會設定 wParam 參數所指定之專案的高度。 否則，此訊息會設定清單方塊中所有專案的高度。
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466524"
---
# <a name="lb_setitemheight-message"></a>LB \_ SETITEMHEIGHT 訊息

設定清單方塊中專案的高度（以圖元為單位）。 如果清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式，則此訊息會設定 *wParam* 參數所指定之專案的高度。 否則，此訊息會設定清單方塊中所有專案的高度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

在清單方塊中指定專案的索引（以零為基底）。 只有在清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式時，才使用此參數; 否則，請將它設定為零。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

指定專案的高度（以圖元為單位）。 最大高度為255圖元。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果索引或高度無效，則傳回值為 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)
</dt> </dl>

 

 





