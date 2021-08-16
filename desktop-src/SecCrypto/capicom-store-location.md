---
description: 指出憑證存放區的位置。
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: 'CAPICOM_STORE_LOCATION 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 15aa93b70840e13901f88c40c715024ec33a835be14b7453da99aecae079b487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879008"
---
# <a name="capicom_store_location-enumeration"></a>CAPICOM \_ 存放區 \_ 位置列舉

**CAPICOM \_ 存放區 \_ 位置** 列舉型別指出 [*憑證存放區*](../secgloss/c-gly.md)的位置。

## <a name="members"></a>成員



| member                                      | 描述                                                                                                                                                                                                                                                                      | 值 |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ 記憶體 \_ 存放區**                  | 存放區是記憶體存放區。 存放區內容中的任何變更都不會保存。<br/>                                                                                                                                                                              | 0     |
| **CAPICOM \_ 本機 \_ 電腦 \_ 存放區**          | 存放區是本機電腦存放區。 只有當使用者擁有讀取/寫入權限時，本機電腦存放區才能成為讀取/寫入存放區。 如果使用者具有讀取/寫入權限，且存放區已開啟讀取/寫入，則會保存存放區內容中的變更。<br/> | 1     |
| **CAPICOM \_ 目前的 \_ 使用者 \_ 存放區**           | 存放區是目前的使用者存放區。 目前的使用者存放區可能是「讀取/寫入」存放區。 如果是，就會保存存放區內容中的變更。<br/>                                                                                                                      | 2     |
| **CAPICOM \_ ACTIVE \_ DIRECTORY \_ 使用者 \_ 存放區** | 存放區是 Active Directory 存放區。 Active Directory 存放區只能在唯讀模式中開啟。 憑證無法在 Active Directory 存放區中新增或移除。<br/>                                                                                        | 3     |
| **CAPICOM \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區**       | 存放區支援以智慧卡為基礎的憑證存放區。 存放區是一組目前的智慧卡。 在 CAPICOM 2.0 中引進。<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>備註

下列方法會使用 **CAPICOM \_ 存放區 \_ 位置** 列舉類型：

-   [**PrivateKey。開啟**](privatekey-open.md)
-   [**Store. Open**](store-open.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
