---
description: 抓取根交易內容中所裝載之交易的隔離等級和超時值。
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: ICoNtextTransactionInfo：： GetTxIsolationLevelAndTimeout 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: 41888a859b6b665390290ba66bed69418cbddd9b708355dc78cc2670ba4d240f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896078"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>ICoNtextTransactionInfo：： GetTxIsolationLevelAndTimeout 方法

抓取根交易內容中所裝載之交易的隔離等級和超時值。

## <a name="syntax"></a>語法


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pIsoLevel* \[擴展\]
</dt> <dd>

交易的 [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) 值。

</dd> <dt>

*dwTime* \[擴展\]
</dt> <dd>

交易的時間（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期和 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

