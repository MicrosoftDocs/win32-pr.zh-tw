---
description: 指定智慧卡上目錄的存取控制許可權。
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: 'CARD_DIRECTORY_ACCESS_CONDITION 列舉 (Cardmod.h .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 8038179c7337edaff0138fc46c34191f99821250808c4ace16dc76cdfafd3b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878958"
---
# <a name="card_directory_access_condition-enumeration"></a>卡片 \_ 目錄 \_ 存取 \_ 條件列舉

**卡片 \_ 目錄 \_ 存取 \_ 條件** 列舉會指定 [*智慧卡*](../secgloss/s-gly.md)上目錄的存取控制許可權。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

此值無效。

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**
</dt> <dd>

特定使用者可以讀取、寫入及刪除目錄。

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**
</dt> <dd>

系統管理員可以讀取、寫入及刪除目錄。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsxp、Windows xp \[ desktop 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windowsserver 2003、Windows server 2003 \[ desktop 應用程式\]<br/>            |
| 標頭<br/>                   | <dl> <dt>Cardmod.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Microsoft 基礎智慧卡密碼編譯服務提供者](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**CardCreateDirectory**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**CardDeleteDirectory**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
