---
title: 'CCM_GETVERSION 訊息 (Commctrl .h) '
description: 取得最新的 CCM SETVERSION 訊息之控制項集的版本號碼 \_ 。
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ad49ebb00d5d57555bb07be1bcf78ab97115ada43e18a7f81cda93e29fa1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320258"
---
# <a name="ccm_getversion-message"></a>CCM \_ GETVERSION 訊息

取得最新的 [**CCM \_ SETVERSION**](ccm-setversion.md) 訊息之控制項集的版本號碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回最新的 [**CCM \_ SETVERSION**](ccm-setversion.md) 訊息所設定的版本號碼。 如果沒有傳送這類訊息，則會傳回零。

## <a name="remarks"></a>備註

此訊息不會傳回 DLL 版本。 請參閱 [Shell 版本](common-control-versions.md) ，以取得如何使用 [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 來取得目前 DLL 版本的討論。

> [!Note]  
> 版本號碼是以控制項為基礎設定的，而且所有控制項都可能不相同。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

