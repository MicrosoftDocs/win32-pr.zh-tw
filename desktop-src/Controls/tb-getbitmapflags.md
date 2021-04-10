---
title: 'TB_GETBITMAPFLAGS 訊息 (Commctrl .h) '
description: 抓取描述要使用之點陣圖類型的旗標。
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106602"
---
# <a name="tb_getbitmapflags-message"></a>TB \_ GETBITMAPFLAGS 訊息

抓取描述要使用之點陣圖類型的旗標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，描述應該使用的點陣圖類型。 如果此傳回值已設定 TBBF \_ 大型旗標，則應用程式應該使用大型點陣圖 (24 x 24) ; 否則，應用程式應該使用小型點陣圖 (16 x 16) 。 所有其他位都是保留的。

## <a name="remarks"></a>備註

**TB \_ GETBITMAPFLAGS** 所傳回的值只是諮詢。 工具列控制項會根據使用者選擇的是大型或小型字型來建議大型或小型點陣圖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





