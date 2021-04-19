---
description: 指定網路來源偵測到的封包配對頻寬和執行時間頻寬。
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: 'MFNETSOURCE_PPBANDWIDTH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979758"
---
# <a name="mfnetsource_ppbandwidth-property"></a>MFNETSOURCE \_ PPBANDWIDTH 屬性

指定網路來源偵測到的封包配對頻寬和執行時間頻寬。 屬性值是兩個值的陣列：

-   封包配對頻寬（以每秒位數為單位）。
-   執行時間頻寬（以位/秒為單位）。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**ULONG** 值的陣列 (**CAUL**) 

VT \_ 向量 \| vt \_ UI4

**科爾**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PPBANDWIDTH** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

這是唯讀的屬性。 若要取得這個屬性，請查詢 **IPropertyStore** 介面的網路來源，然後呼叫 **IPropertyStore：： GetValue**。

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

 

 




