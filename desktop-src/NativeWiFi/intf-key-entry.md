---
description: 儲存無線設定服務所管理的無線區域網路介面相關的重要資訊。
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: 'INTF_KEY_ENTRY 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 8d14c65d49d7ed28e2756c2a690cb4a7efa9000417e896a206710bf4365f8cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065148"
---
# <a name="intf_key_entry-structure"></a>INTF \_ \_ 索引鍵輸入結構

\[**INTF \_不再 \_** 支援 Windows Vista 和 Windows Server 2008 的金鑰輸入。 相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

**INTF 機 \_ 碼 \_ 輸入** 結構會儲存無線設定服務所管理的無線區域網路介面相關的重要資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**wszGuid**
</dt> <dd>

以下列格式的 Unicode 字串形式表示之介面 GUID 的指標： "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"。

</dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | WindowsXP SP3<br/>                                                       |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Wzcsapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INTFS 索引 \_ 鍵 \_ 資料表**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




