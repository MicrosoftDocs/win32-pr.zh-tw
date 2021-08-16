---
title: 'TBM_GETLINESIZE 訊息 (Commctrl .h) '
description: 抓取捲軸滑動軸移動以回應鍵盤輸入的邏輯位置數目，例如，或索引鍵。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6db69efda8a6836f8c366092871cbb6b54261021a69c80e2bb14abcd88d967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046558"
---
# <a name="tbm_getlinesize-message"></a>TBM \_ GETLINESIZE 訊息

抓取捲軸滑動軸移動以回應鍵盤輸入的邏輯位置數目，例如，或索引鍵。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回32位的值，這個值會指定列的行大小。

## <a name="remarks"></a>備註

行大小的預設設定為1。

當使用者按下方向鍵時，此項資訊也會將具有 TB 組合和 TB LINEDOWN 通知碼的 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送 \_ \_ 至其父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





