---
title: 'INapClientManagement2 GetSystemIsolationInfoEx 方法 (NapManagement .h) '
description: 抓取 NapClient 的隔離狀態和擴充隔離狀態的相關資訊。
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- GetSystemIsolationInfoEx 方法 NAP
- GetSystemIsolationInfoEx 方法 NAP，INapClientManagement2 介面
- INapClientManagement2 介面 NAP，GetSystemIsolationInfoEx 方法
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03630cbd0647dc177460f92abc28e6aa66cbb663465ba7e9e93eefbc283ac00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621925"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>INapClientManagement2：： GetSystemIsolationInfoEx 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetSystemIsolationInfoEx** 方法會抓取 NapClient 的隔離狀態和擴充隔離狀態的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*isolationInfo* \[擴展\]
</dt> <dd>

[**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構指標的指標，其中包含隔離狀態資訊。

</dd> <dt>

*unknownConnections* \[擴展\]
</dt> <dd>

布林值的指標，如果有任何連接處於未知狀態，則為 **TRUE** ，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。



| 傳回碼                                                                                         | 描述                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**RPC \_ E \_ 中斷連接**</dt> </dl> | NapAgent 未執行。<br/>                            |



 

## <a name="remarks"></a>備註

抓取的隔離資訊不會反映不明的狀態。

SHA 必須藉由呼叫 [**FreeIsolationInfoEx**](freeisolationinfoex.md)來釋放 [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>NapManagement。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





