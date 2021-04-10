---
title: ITsSbTaskInfo 內容屬性
description: 捕獲與工作相關聯的內容位元組。
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- 內容屬性遠端桌面服務
- CoNtext 屬性遠端桌面服務，ITsSbTaskInfo 介面
- ITsSbTaskInfo 介面遠端桌面服務、內容屬性
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106085"
---
# <a name="itssbtaskinfocontext-property"></a>ITsSbTaskInfo：： CoNtext 屬性

捕獲與工作相關聯的內容位元組。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a>屬性值

工作的內容。

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

 

 





