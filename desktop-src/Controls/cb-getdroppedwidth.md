---
title: 'CB_GETDROPPEDWIDTH 訊息 (Winuser .h) '
description: 取得具有 CBS \_ 下拉式清單或 cbs DROPDOWNLIST 樣式之下拉式方塊清單方塊的最小允許寬度（以圖元為單位） \_ 。
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- CB_GETDROPPEDWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025094"
---
# <a name="cb_getdroppedwidth-message"></a>CB \_ GETDROPPEDWIDTH 訊息

取得具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式之下拉式方塊清單方塊的最小允許寬度（以圖元為單位）。

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

如果訊息成功，則傳回值為寬度（以圖元為單位）。

如果訊息失敗，則傳回值為 CB \_ ERR。

## <a name="remarks"></a>備註

根據預設，下拉式清單方塊的最小允許寬度為零。 清單方塊的寬度可以是允許的最小寬度或下拉式方塊寬度（以較大者為准）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





