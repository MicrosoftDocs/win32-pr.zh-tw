---
title: ITsSbSession Username 屬性
description: 抓取此會話的使用者名稱。
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Username 屬性遠端桌面服務
- Username 屬性遠端桌面服務，ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，使用者名稱屬性
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966349"
---
# <a name="itssbsessionusername-property"></a>ITsSbSession：： Username 屬性

抓取此會話的使用者名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a>屬性值

接收此會話之使用者名稱之 **BSTR** 變數的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





