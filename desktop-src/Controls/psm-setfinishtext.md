---
title: 'PSM_SETFINISHTEXT 訊息 (Prsht.idl .h) '
description: 設定 wizard 中 [完成] 按鈕的文字、顯示並啟用按鈕，以及隱藏 [下一步] 和 [上一頁] 按鈕。 您可以使用 PropSheet SetFinishText 宏明確地傳送此訊息 \_ 。
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685557"
---
# <a name="psm_setfinishtext-message"></a>PSM \_ SETFINISHTEXT 訊息

設定 wizard 中 [ **完成]** 按鈕的文字、顯示並啟用按鈕，以及隱藏 [ **下一步]** 和 [ **上一頁** ] 按鈕。 您可以使用 [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[ **完成]** 按鈕的新文字指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

依預設，[ **完成]** 按鈕沒有鍵盤快速鍵。 您可以使用此訊息建立鍵盤快速鍵，方法是在您指派給 *lParam* 的文字字串中包含連字號 (&) 。 例如，「&完成」會將 F 定義為快速鍵。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **PSM \_SETFINISHTEXTW** (Unicode) 和 **PSM \_ SETFINISHTEXTA** (ANSI) <br/>    |



 

 





