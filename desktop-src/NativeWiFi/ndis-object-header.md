---
description: 封裝許多 NDIS 6.0 結構中所需的物件類型、版本和大小資訊。
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: 'NDIS_OBJECT_HEADER 結構 (Ntddndis .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983482"
---
# <a name="ndis_object_header-structure"></a>NDIS \_ 物件 \_ 標頭結構

**Ndis \_ 物件 \_ 標頭** 結構會封裝許多 NDIS 6.0 結構中所需的物件類型、版本和大小資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**型別**
</dt> <dd>

指定結構所描述之 NDIS 物件的型別。

</dd> <dt>

**修訂**
</dt> <dd>

指定此結構的修訂編號。

</dd> <dt>

**大小**
</dt> <dd>

指定包含 **ndis \_ 物件 \_ 標頭** 之 ndis 結構的總大小（以位元組為單位）。 此大小包含 **NDIS \_ 物件 \_ 標頭** 成員的大小，以及結構的所有其他成員。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                       |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Ntddndis (包含 Windot11) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DOT11 \_ BSSID \_ 清單**](dot11-bssid-list.md)
</dt> </dl>

 

 




