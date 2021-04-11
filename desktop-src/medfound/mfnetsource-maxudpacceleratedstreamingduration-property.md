---
description: 當網路來源使用 UDP 傳輸時，加速資料流程的最長持續時間（以毫秒為單位）。
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: 'MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027425"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a>MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION 屬性

當網路來源使用 UDP 傳輸時，加速資料流程的最長持續時間（以毫秒為單位）。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**DWORD** (儲存為 **LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

若是 UDP 傳輸，如果這個屬性的值較低，這個屬性會覆寫 [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) 屬性。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

這個屬性的預設值為8000毫秒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[網路來源功能](network-source-features.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




