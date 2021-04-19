---
description: 指定智慧卡上檔案的存取控制許可權。
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: 'CARD_FILE_ACCESS_CONDITION 列舉 (Cardmod.h .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991707"
---
# <a name="card_file_access_condition-enumeration"></a>卡片 \_ 檔案 \_ 存取 \_ 條件列舉

**卡片檔案 \_ \_ 存取 \_ 條件** 列舉會指定 [*智慧卡*](../secgloss/s-gly.md)上檔案的存取控制許可權。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

此值無效。

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**
</dt> <dd>

每個人都可以讀取檔案。 特定使用者可以寫入檔案。

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

只有特定使用者可以讀取或寫入檔案。

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

每個人都可以讀取檔案。 系統管理員可以寫入檔案。

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

檔案的存取權限不明。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows XP、Windows XP \[ desktop 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | 僅限 windows Server 2003、Windows Server 2003 \[ desktop 應用程式\]<br/>            |
| 標頭<br/>                   | <dl> <dt>Cardmod.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Microsoft 基礎智慧卡密碼編譯服務提供者](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**卡片 \_ 檔案 \_ 資訊**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
