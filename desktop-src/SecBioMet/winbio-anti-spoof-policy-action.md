---
title: 'WINBIO_ANTI_SPOOF_POLICY_ACTION 列舉 (Winbio \_ 類型 .h) '
description: 指定您針對使用者的 lnk-antispoofing 原則所採取的動作類型。
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION 列舉 Windows 生物特徵辨識架構 API
- PWINBIO_ANTI_SPOOF_POLICY 列舉指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65fec198a0784bf076eb90224318bd36a88ba3ed96258ffd2014a27da5c8f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911267"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作列舉

指定您針對使用者的 lnk-antispoofing 原則所採取的動作類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ 反 \_ 欺騙 \_ 停用**
</dt> <dd>

關閉生物識別因素的詐騙偵測。

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ 反 \_ 詐騙 \_ 啟用**
</dt> <dd>

開啟生物識別因素的詐騙偵測。

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO \_ 消除 \_ 詐騙 \_ 移除**
</dt> <dd>

從帳戶中移除生物特徵辨識因素的整個 lnk-antispoofing 原則。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**WINBIO \_ 原則 \_ 來源**](winbio-policy-source.md)
</dt> </dl>

 

 





