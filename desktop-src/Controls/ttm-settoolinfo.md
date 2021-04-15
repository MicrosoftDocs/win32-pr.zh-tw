---
title: 'TTM_SETTOOLINFO 訊息 (Commctrl .h) '
description: 設定工具提示控制項為工具維護的資訊。
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- TTM_SETTOOLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466797"
---
# <a name="ttm_settoolinfo-message"></a>TTM \_ SETTOOLINFO 訊息

設定工具提示控制項為工具維護的資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，指定要設定的資訊。 傳送此訊息之前，必須先設定此結構的 **cbSize** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

工具的某些內部屬性會在建立工具時建立，而且在傳送 **TTM \_ SETTOOLINFO** 訊息時不會重新計算。 如果您只是將值指派給 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構，並將其傳遞至具有 **TTM \_ SETTOOLINFO** 訊息的工具提示控制項，這些屬性可能會遺失。 相反地，您的應用程式應該先傳送工具提示控制項 a [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md)訊息，以要求工具目前的 **TOOLINFO** 結構。 然後，視需要修改此結構的成員，並將其傳遞回具有 **TTM \_ SETTOOLINFO** 的工具提示控制項。

呼叫 **TTM \_ SETTOOLINFO** 時， [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **lpszText** 成員所指向的字串不得超過 80 **TCHARs** 的長度，包括終止的 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_SETTOOLINFOW** (Unicode) 和 **TTM \_ SETTOOLINFOA** (ANSI) <br/>           |



 

 





