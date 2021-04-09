---
title: 'LB_SETLOCALE 訊息 (Winuser .h) '
description: 設定清單方塊的目前地區設定。 您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有磅 \_ 排序樣式) 的清單方塊，以及 LB ADDSTRING 訊息所加入的文字 \_ 。
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025380"
---
# <a name="lb_setlocale-message"></a>LB \_ SETLOCALE 訊息

設定清單方塊的目前地區設定。 您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有 [**磅 \_ 排序**](list-box-styles.md) 樣式) 的清單方塊，以及 [**LB \_ ADDSTRING**](lb-addstring.md) 訊息所加入的文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定當加入文字時，清單方塊將用來排序的地區設定識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是先前的地區設定識別碼。 如果 *wParam* 參數指定的地區設定未安裝在系統上，則傳回值為 LB \_ ERR，而且目前的清單方塊地區設定不會變更。

## <a name="remarks"></a>備註

使用 [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼。

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETLOCALE**](lb-getlocale.md)
</dt> </dl>

 

