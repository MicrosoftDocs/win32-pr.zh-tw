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
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970551"
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
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

