---
title: 'CB_GETLBTEXT 訊息 (Winuser .h) '
description: 從下拉式方塊的清單中取得字串。
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- CB_GETLBTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025089"
---
# <a name="cb_getlbtext-message"></a>CB \_ GETLBTEXT 訊息

從下拉式方塊的清單中取得字串。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要抓取之字串的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

接收字串的緩衝區指標。 緩衝區必須有足夠的空間可供字串和終止的 null 字元使用。 您可以在 **cb \_ GETLBTEXT** 訊息之前傳送 [**cb \_ GETLBTEXTLEN**](cb-getlbtextlen.md)訊息，以取得字串的長度（以 **TCHAR** s 為限）。 如果是 ANSI 字串，則這是位元組的數目，但如果它是 Unicode 字串，則這是字元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是字串的長度（在 **TCHAR** s 中），不包括結束的 null 字元。 如果 *wParam* 未指定有效的索引，則傳回值為 CB \_ ERR。

## <a name="remarks"></a>備註

**安全性警告：** 不當使用此訊息可能會危及程式的安全性。 此訊息不會提供您知道緩衝區大小的方法。 如果您使用此訊息，請先呼叫 [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) 來取得所需的字元數，然後呼叫訊息以取得字串。 您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。

如果您建立具有主控描繪樣式的下拉式方塊，但沒有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，則 *lParam* 所指向的緩衝區會接收與該專案相關聯的資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
</dt> </dl>

 

 





