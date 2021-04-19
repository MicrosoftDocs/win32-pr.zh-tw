---
title: Win32_RDMSJoinedNode 類別的 GetJoinedNodeCount 方法
description: 取得已安裝指定角色的伺服器數目。
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- GetJoinedNodeCount 方法遠端桌面服務
- GetJoinedNodeCount 方法遠端桌面服務，Win32_RDMSJoinedNode 類別
- Win32_RDMSJoinedNode 類別遠端桌面服務，GetJoinedNodeCount 方法
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966305"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a>Win32 RDMSJoinedNode 類別的 GetJoinedNodeCount 方法 \_

取得已安裝指定角色的伺服器數目。

## <a name="syntax"></a>語法


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*roleType* \[在\]
</dt> <dd>

指定角色類型的位位。

<dt>

0
</dt> <dd>

全部

</dd> <dt>

1
</dt> <dd>

遠端桌面連線代理人 (RDCB) 

</dd> <dt>

2
</dt> <dd>

遠端桌面工作階段主機 (RDSH) 

</dd> <dt>

4
</dt> <dd>

遠端桌面虛擬化主機 (RDVH) 

</dd> </dl> </dd> <dt>

*計數* \[擴展\]
</dt> <dd>

成功時，會傳回已安裝指定角色的伺服器數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





