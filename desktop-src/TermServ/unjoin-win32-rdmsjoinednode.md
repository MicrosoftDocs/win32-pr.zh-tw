---
title: Win32_RDMSJoinedNode 類別的退出方法
description: 從遠端桌面管理服務 (RDMS) 移除節點。
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- 退出方法遠端桌面服務
- 退出方法遠端桌面服務，Win32_RDMSJoinedNode 類別
- Win32_RDMSJoinedNode 類別遠端桌面服務、退出方法
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d2fae16ecb31326ae16bc08efd1fbc56ae2585140d63ce360783226101d4a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424098"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Win32 RDMSJoinedNode 類別的退出方法 \_

從遠端桌面管理服務 (RDMS) 移除節點。

## <a name="syntax"></a>語法


```mof
uint32 Unjoin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

 

 





