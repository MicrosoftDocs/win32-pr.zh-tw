---
title: 'LM_GETIDEALSIZE 訊息 (Commctrl .h) '
description: LM_GETIDEALSIZE 訊息-針對控制項目前寬度的連結，取得其慣用高度。
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035a919aabeb5d07587c7d9e4fc97e5edc728de4ec8fc476448dca62658f1ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958369"
---
# <a name="lm_getidealsize-message"></a>LM \_ GETIDEALSIZE 訊息

抓取控制項目前寬度之連結的慣用高度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>連結的最大寬度（以圖元為單位）。</dd> <dt>

*lParam* \[擴展\]
</dt> <dd>當這個訊息傳回時，會包含 <a href="/previous-versions//dd145106(v=vs.85)">**大小**</a> 結構的指標。 此結構的 **cy** 成員表示指定寬度之控制項的理想高度。 它會將 **cx** 成員調整為實際需要的空間量。</dd> </dl>

## <a name="return-value"></a>傳回值

整數，表示連結文字的慣用高度（以圖元為單位）。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

