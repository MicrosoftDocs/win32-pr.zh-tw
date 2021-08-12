---
title: Win32_RDMSJoinedNode 類別的 Join 方法
description: 將節點新增至遠端桌面管理服務 (RDM) 。
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Join 方法遠端桌面服務
- Join 方法遠端桌面服務，Win32_RDMSJoinedNode 類別
- Win32_RDMSJoinedNode 類別遠端桌面服務，Join 方法
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204d83988f9a57d9fe0edf8daa6dc580676fc7395f98edcbece49674c0041aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605421"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Win32 RDMSJoinedNode 類別的 Join 方法 \_

將節點新增至遠端桌面管理服務 (RDM) 。

## <a name="syntax"></a>語法


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NodeFQDN* \[在\]
</dt> <dd>

節點的完整功能變數名稱。

</dd> <dt>

*NodeSID* \[在\]
</dt> <dd>

節點 (SID) 的安全識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





