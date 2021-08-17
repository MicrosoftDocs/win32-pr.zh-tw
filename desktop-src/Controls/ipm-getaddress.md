---
title: 'IPM_GETADDRESS 訊息 (Commctrl .h) '
description: 取得 IP 位址控制項中所有四個欄位的位址值。
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bcb35ed71532e815b33b45e1c15e9b82b75b5c87fac406b52de80670e3d72a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434509"
---
# <a name="ipm_getaddress-message"></a>IPM \_ GETADDRESS 訊息

取得 IP 位址控制項中所有四個欄位的位址值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

接收位址之 **DWORD** 值的指標。 欄位3值會包含在位0到7。 欄位2值會包含在位8到15之間。 欄位1值會包含在位16到23之間。 欄位0值將包含在位24到31之間。 [**第一個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)、[**第二個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)、[**第三個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)和 [**第四個 \_ ipaddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress)宏也可以用來解壓縮位址資訊。 零會以任何空白欄位的位址傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非空白欄位的數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





