---
title: 'TTM_ENUMTOOLS 訊息 (Commctrl .h) '
description: 抓取工具提示控制項針對目前工具 \ 郵件所維護的資訊，也就是工具提示目前顯示文字的工具。
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465357"
---
# <a name="ttm_enumtools-message"></a>TTM \_ ENUMTOOLS 訊息

抓取工具提示控制項針對目前工具所維護的資訊，也就是工具提示目前顯示文字的工具。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的工具索引，用來取得資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，此結構會接收工具的相關資訊。 將此結構的 **cbSize** 成員設定為 SIZEOF (TOOLINFO) ，然後再傳送此訊息。 配置緩衝區。 設定 **lpszText** 成員指向緩衝區以接收工具文字。 沒有任何方法可判斷所需的緩衝區大小。 不過，在 **TOOLINFO** 結構的 **lpszText** 成員上傳回的工具文字具有最大長度 80 **TCHARs**，包括終止的 **Null**。 如果文字超過此長度，則會被截斷。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果列舉任何工具，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

**安全性警告：** 使用此訊息可能會危害程式的安全性。 這則訊息不會提供訊息接收者知道緩衝區大小或指定緩衝區大小的方法。 您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_ENUMTOOLSW** (Unicode) 和 **TTM \_ ENUMTOOLSA** (ANSI) <br/>               |



 

 





