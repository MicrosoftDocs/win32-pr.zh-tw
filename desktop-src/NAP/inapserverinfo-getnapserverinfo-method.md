---
title: 'INapServerInfo GetNapServerInfo 方法 (NapServerManagement .h) '
description: 抓取 NAP 伺服器的相關資訊。
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- GetNapServerInfo 方法 NAP
- GetNapServerInfo 方法 NAP，INapServerInfo 介面
- INapServerInfo 介面 NAP，GetNapServerInfo 方法
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eec9926e1a0bf94a1e3dac38c01a169d596c1c00bf032b8f6954f6331d5a4d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626128"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>INapServerInfo：： GetNapServerInfo 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapServerInfo：： GetNapServerInfo** 方法會抓取 NAP 伺服器的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*serverName* \[擴展\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含伺服器名稱。

</dd> <dt>

*serverDescription* \[擴展\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含伺服器描述。

</dd> <dt>

*protocolVersion* \[擴展\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含通訊協定版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapServerManagement。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





