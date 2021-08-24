---
title: 'INapClientManagement RegisterSystemHealthAgent 方法 (NapManagement .h) '
description: 向 NAP 系統註冊 SHA。
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- RegisterSystemHealthAgent 方法 NAP
- RegisterSystemHealthAgent 方法 NAP，INapClientManagement 介面
- INapClientManagement 介面 NAP，RegisterSystemHealthAgent 方法
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e028e1f3dab17fb154ad1676acbf14fe1a31ce69a8f4c511e7f1447d2303bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803148"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>INapClientManagement：： RegisterSystemHealthAgent 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**RegisterSystemHealthAgent** 方法會向 NAP 系統註冊 SHA。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*代理程式* \[在\]
</dt> <dd>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構的指標，其中包含 SHA 的註冊資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 HRESULT 狀態碼，包括但不限於下列其中一項。



| 傳回碼                                                                                            | 描述                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 衝突 \_ 識別碼**</dt> </dl> | 使用此識別碼的 SHA 已經註冊。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>NapManagement。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





