---
description: 網路來源加速資料流程的持續時間（以毫秒為單位）。
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: 'MFNETSOURCE_ACCELERATEDSTREAMINGDURATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ec37cfd7dd0aa8d60c3e192ae0f445f8a121e9e3cd3f85d46e8c18b21fc2b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243862"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION 屬性

網路來源加速資料流程的持續時間（以毫秒為單位）。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**DWORD** (儲存為 **LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 物件傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

這個屬性會套用至 Windows Media Services 的快速啟動功能，此功能可快速播放內容，而不會等候冗長的初始緩衝。 使用 [快速啟動] 時，執行 Windows Media Services 的伺服器會以比內容位元速率所指定更快的速度，傳送內容開頭的一些資料。

這個屬性的預設值為10000毫秒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[網路來源功能](network-source-features.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




