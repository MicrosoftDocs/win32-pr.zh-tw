---
title: 'CBEM_HASEDITCHANGED 訊息 (Commctrl .h) '
description: 判斷使用者是否已變更 ComboBoxEx 編輯控制項的文字。
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5949827dbabf962ec9a9e9bd9d3b6d27d09a3b7e62f7fc71f2c4343e8ce370
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528038"
---
# <a name="cbem_haseditchanged-message"></a>CBEM \_ HASEDITCHANGED 訊息

判斷使用者是否已變更 ComboBoxEx 編輯控制項的文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果控制項編輯方塊中的文字已變更，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

當 ComboBoxEx 控制項設定為 [**CBS \_ 下拉式**](combo-box-styles.md) 樣式時，會使用編輯方塊控制項。 您可以藉由傳送 [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) 訊息來取得編輯方塊控制項的視窗控制碼。

當使用者開始編輯時，您將會收到 [CBEN \_ BEGINEDIT](cben-beginedit.md) 通知。 當編輯完成或焦點變更時，您將會收到 [CBEN \_ ENDEDIT](cben-endedit.md) 通知。 **CBEM \_ HASEDITCHANGED** 訊息只適用于在 CBEN ENDEDIT 通知之前，判斷文字是否已變更 \_ 。 如果訊息在之後傳送，則會傳回 **FALSE**。 例如，假設使用者開始編輯編輯方塊中的文字，但變更焦點，產生 CBEN \_ ENDEDIT 通知。 如果您接著傳送 **CBEM \_ HASEDITCHANGED** 訊息，它會傳回 **FALSE**，即使文字已變更也是一樣。

[**CBS \_ 簡單**](combo-box-styles.md)樣式無法與 **CBEM \_ HASEDITCHANGED** 正常搭配運作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





