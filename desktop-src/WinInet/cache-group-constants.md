---
title: '快取群組常數 (Wininet. h) '
description: 下列清單包含快取群組函數所使用的常數。
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967755"
---
# <a name="cache-group-constants"></a>快取群組常數

下列清單包含快取群組函數所使用的常數。

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP \_ 屬性 \_ 基本**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



抓取快取群組的旗標、類型和磁片配額屬性。 [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP \_ 屬性 \_ 旗標**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



設定或抓取與快取群組相關聯的旗標。 [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP \_ 屬性 \_ 取得 \_ 全部**
</dt> <dd> <dl> <dt>

0xffffffff
</dt> <dt>



抓取快取群組的所有屬性。 [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP \_ 屬性的屬性 \_**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



設定或抓取快取群組的組名。 [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP \_ 屬性 \_ 配額**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



設定或抓取與快取群組相關聯的磁片配額。 [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP \_ 屬性 \_ 儲存體**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



設定或抓取與快取群組相關聯的群組擁有者儲存體。 [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP \_ 屬性 \_ 類型**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



設定或抓取快取群組類型。 [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)和 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP \_ 旗標 \_ FLUSHURL \_ ONDELETE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



表示應該刪除與快取群組相關聯的所有快取專案，除非該專案屬於另一個快取群組。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP \_ 旗標 \_ GIDONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



指出函式應該只為快取群組建立唯一的 GROUPID，而不是建立實際的群組。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP \_ 旗標 \_ NONPURGEABLE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



表示無法清除快取群組。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP \_ READWRITE \_ 遮罩**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



設定快取群組的類型、磁片配額、組名和擁有者儲存體屬性。 [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)函式會使用這項功能。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ 搜尋 \_ 全部**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



表示應該列舉使用者系統中的所有快取群組。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ 搜尋 \_ BYURL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



目前未實作。


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP \_ 類型 \_ 無效**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



指出快取群組類型無效。


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**群組 \_ 擁有者 \_ 儲存體 \_ 大小**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



群組擁有者儲存陣列的長度。


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**具有 \_ 最大長度的各名 \_**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



快取組名允許的最大字元數。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wininet</dt> </dl> |



 

