---
title: ITsSbTaskInfo Status 屬性
description: 抓取 RDV 工作 \_ \_ 狀態列舉值，這個值表示工作的狀態。
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Status 屬性遠端桌面服務
- Status 屬性遠端桌面服務，ITsSbTaskInfo 介面
- ITsSbTaskInfo 介面遠端桌面服務，Status 屬性
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685860"
---
# <a name="itssbtaskinfostatus-property"></a>ITsSbTaskInfo：： Status 屬性

抓取 [**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) 列舉值，這個值表示工作的狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a>屬性值

[**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)列舉值，表示工作的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





