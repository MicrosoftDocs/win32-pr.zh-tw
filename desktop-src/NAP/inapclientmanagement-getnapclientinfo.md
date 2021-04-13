---
title: 'INapClientManagement GetNapClientInfo 方法 (NapManagement .h) '
description: 抓取 NAP 用戶端的相關資訊。
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- GetNapClientInfo 方法 NAP
- GetNapClientInfo 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，GetNapClientInfo 方法
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508887"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a>INapClientManagement：： GetNapClientInfo 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetNapClientInfo** 方法會抓取 NAP 用戶端的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*isNapEnabled* \[擴展\]
</dt> <dd>

如果啟用 NAP，則為布林值的指標，設定為 **TRUE** 。否則會設為 **FALSE**。

</dd> <dt>

*clientName* \[擴展\]
</dt> <dd>

指向包含用戶端名稱之 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) 結構指標的指標。

</dd> <dt>

*clientDescription* \[擴展\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含用戶端描述。

</dd> <dt>

*protocolVersion* \[擴展\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含通訊協定版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。



| 傳回碼                                                                                         | Description                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**RPC \_ E \_ 中斷連接**</dt> </dl> | NapAgent 未執行。<br/>                            |



 

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

 

 





