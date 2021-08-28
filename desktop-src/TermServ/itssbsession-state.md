---
title: ITsSbSession 狀態屬性
description: 捕獲或指定會話狀態。
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- State 屬性遠端桌面服務
- State 屬性遠端桌面服務，ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，State 屬性
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d8eef2a19ff9b92f7d860bb17662e84e4028eb21a5a228819b90b0af31ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128168"
---
# <a name="itssbsessionstate-property"></a>ITsSbSession：： State 屬性

捕獲或指定會話狀態。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a>屬性值

[**TSSESSION \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)列舉的值，表示會話的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[**TSSESSION \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





