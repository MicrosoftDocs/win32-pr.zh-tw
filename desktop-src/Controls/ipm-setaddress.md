---
title: 'IPM_SETADDRESS 訊息 (Commctrl .h) '
description: 在 IP 位址控制項中設定所有四個欄位的位址值。
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS message Windows 控制項
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104465"
---
# <a name="ipm_setaddress-message"></a>IPM \_ SETADDRESS 訊息

在 IP 位址控制項中設定所有四個欄位的位址值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** 值，包含新的位址。 欄位3值包含在位0到7。 欄位2值包含在位8到15之間。 欄位1值包含在位16到23之間。 欄位0值包含在位24到31之間。 [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)宏也可以用來建立位址資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

此訊息不會產生 [**IPN \_ FIELDCHANGED**](ipn-fieldchanged.md) 通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





