---
title: 'INapClientManagement GetSystemIsolationInfo 方法 (NapManagement .h) '
description: 抓取 NapClient 隔離狀態的相關資訊。
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- GetSystemIsolationInfo 方法 NAP
- GetSystemIsolationInfo 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，GetSystemIsolationInfo 方法
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385017"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a>INapClientManagement：： GetSystemIsolationInfo 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetSystemIsolationInfo** 方法會抓取 NapClient 的隔離狀態相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*isolationInfo* \[擴展\]
</dt> <dd>

[**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)結構指標的指標，其中包含隔離狀態資訊。

</dd> <dt>

*unknownConnections* \[擴展\]
</dt> <dd>

旗標的指標，指出是否有任何連接處於未知的狀態。 如果有的話，旗標會設為 **TRUE**;否則旗標會設為 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。



| 傳回碼                                                                                         | Description                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**RPC \_ E \_ 中斷連接**</dt> </dl> | NapAgent 未執行。<br/>                            |



 

## <a name="remarks"></a>備註

抓取的隔離資訊不會反映不明的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>NapManagement。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





