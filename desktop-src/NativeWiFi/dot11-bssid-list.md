---
description: 包含基本服務集 (BSS) 識別碼的清單。
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: 'DOT11_BSSID_LIST 結構 (Windot11 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 8abcd2e711d5598c59bb8d4b7aed0f291364f94d04ec17a5fc80de2fd32939eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801388"
---
# <a name="dot11_bssid_list-structure"></a>DOT11 \_ BSSID \_ 清單結構

**DOT11 \_ BSSID \_ 清單** 結構包含基本服務集 (BSS) 識別碼的清單。

## <a name="syntax"></a>語法


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>成員

<dl> <dt>

**標頭**
</dt> <dd>

[**Ndis \_ 物件 \_ 標頭**](ndis-object-header.md)結構，包含 ndis 結構的類型、版本和大小資訊。 對於大部分的 **DOT11 \_ BSSID \_ 清單** 結構，請 **將類型** 成員設定為 **NDIS \_ 物件 \_ 類型 \_ 預設值**、將 **修訂** 成員設定為 **DOT11 \_ BSSID \_ 清單 \_ 修訂版 \_ 1**，然後將 **Size** 成員設為 **sizeof (DOT11 \_ BSSID \_ 清單)**。

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

此結構中的專案數。

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

支援的專案總數。

</dd> <dt>

**BSSIDs**
</dt> <dd>

BSS 識別碼的清單。 BSS 識別碼會儲存為 [**DOT11 \_ MAC \_ 位址**](dot11-mac-address-type.md) 類型。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                       |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Windot11 (包含 Windot11) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WLAN \_ 連接 \_ 參數**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




