---
title: 'EM_GETCUEBANNER 訊息 (Commctrl .h) '
description: 取得在編輯控制項中顯示為文字提示或提示的文字。
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935055"
---
# <a name="em_getcuebanner-message"></a>EM \_ GETCUEBANNER 訊息

取得在編輯控制項中顯示為文字提示或提示的文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

Unicode 緩衝區的指標，此緩衝區會以文字提示的形式接收文字集。 呼叫端負責配置緩衝區。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

*WParam* 在 **WCHARs** 中所指向的緩衝區大小，包括終止的 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯 \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





