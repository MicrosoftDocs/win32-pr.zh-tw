---
title: 'LB_GETITEMHEIGHT 訊息 (Winuser .h) '
description: 取得清單方塊中專案的高度。
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- LB_GETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843432"
---
# <a name="lb_getitemheight-message"></a>LB \_ GETITEMHEIGHT 訊息

取得清單方塊中專案的高度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單方塊專案以零為基底的索引。 只有在清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式時，才會使用此索引; 否則，它必須為零。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是清單方塊中每個專案的高度（以圖元為單位）。 如果清單方塊具有 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md)樣式，則傳回值為 *wParam* 參數所指定之專案的高度。 如果發生錯誤，傳回值會是 LB \_ ERR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)
</dt> </dl>

 

 





