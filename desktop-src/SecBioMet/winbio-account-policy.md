---
title: 'WINBIO_ACCOUNT_POLICY 結構 (Winbio \_ adapter .h) '
description: 包含預設或帳戶特定的 lnk-antispoofing 原則。
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY 結構 Windows 生物特徵辨識架構 API
- PWINBIO_ACCOUNT_POLICY 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c30241f0e13528c8427367c61362b803caaa9fc8c0a15a0eefad72689517d40f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035248"
---
# <a name="winbio_account_policy-structure"></a>WINBIO \_ 帳戶 \_ 原則結構

**WINBIO \_ 帳戶 \_ 原則** 結構包含預設或帳戶特定的 lnk-antispoofing 原則。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a>成員

<dl> <dt>

**身分識別**
</dt> <dd>

指定帳戶資訊的 [**WINBIO 身分 \_ 識別**](winbio-identity.md) 結構。

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

其中一個 [**WINBIO \_ 反詐騙 \_ \_ 原則 \_ 動作**](winbio-anti-spoof-policy-action.md) 列舉值，指定要對帳戶使用哪個 lnk-antispoofing 原則動作。

</dd> </dl>

## <a name="remarks"></a>備註

如需如何使用此結構的說明，請參閱 [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) 方法的討論。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ adapter .h (包括 Winbio \_ adapter .h) </dt> </dl> |



 

 





