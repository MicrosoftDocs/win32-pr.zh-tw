---
description: 包含無線設定服務所管理之所有無線區域網路介面的重要資訊表格。
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: 'INTFS_KEY_TABLE 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971429"
---
# <a name="intfs_key_table-structure"></a>INTFS 索引 \_ 鍵 \_ 資料表結構

\[**INTFS \_Windows \_** Vista 和 windows Server 2008 不再支援索引鍵資料表。 相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

**INTFS 索引 \_ 鍵 \_ 資料表** 結構包含無線設定服務所管理之所有無線區域網路介面的重要資訊表格。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**dwNumIntfs**
</dt> <dd>

介面的總數目。

</dd> <dt>

**pIntfs**
</dt> <dd>

[**INTF \_ \_ 索引鍵輸入**](intf-key-entry.md)結構的指標。

</dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | Windows XP （含 SP3）<br/>                                                       |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Wzcsapi。h</dt> </dl> |



 

 




