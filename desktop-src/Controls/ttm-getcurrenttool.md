---
title: 'TTM_GETCURRENTTOOL 訊息 (Commctrl .h) '
description: 抓取工具提示控制項中目前工具的資訊。
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934398"
---
# <a name="ttm_getcurrenttool-message"></a>TTM \_ GETCURRENTTOOL 訊息

抓取工具提示控制項中目前工具的資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，此結構會接收目前工具的相關資訊。 如果這個值為 **Null**，則傳回值會指出目前的工具是否存在，而不會實際抓取工具資訊。 如果這個值不是 **Null**，則必須先填入 **TOOLINFO** 結構的 **cbSize** 成員，才能傳送此訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。 如果 *lParam* 為 **Null**，則傳回非零值（如果目前的工具存在），否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_GETCURRENTTOOLW** (Unicode) 和 **TTM \_ GETCURRENTTOOLA** (ANSI) <br/>     |



 

 





