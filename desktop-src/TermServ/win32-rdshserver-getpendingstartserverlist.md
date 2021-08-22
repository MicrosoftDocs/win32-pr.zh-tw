---
title: Win32_RDSHServer 類別的 GetPendingStartServerList 方法
description: 抓取等候啟動的伺服器清單。
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- GetPendingStartServerList 方法遠端桌面服務
- GetPendingStartServerList 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，GetPendingStartServerList 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61bb46512414c7057d7ec9db5ff4b6fab859f8bb9e6aec5c537250b0baa24e9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422648"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Win32 RDSHServer 類別的 GetPendingStartServerList 方法 \_

抓取等候啟動的伺服器清單。

## <a name="syntax"></a>語法


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*maxServers* \[在\]
</dt> <dd>

要在清單中傳回的最大伺服器數目。

</dd> <dt>

*ServerFQDNs* \[擴展\]
</dt> <dd>

成功時，會包含等待啟動之伺服器的完整功能變數名稱集合。

</dd> </dl>

## <a name="remarks"></a>備註

伺服器清單會在每次呼叫之後重設，讓下一個呼叫不會收到重複的伺服器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





