---
description: 網路來源緩衝的最大資料量（以毫秒為單位）。
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: 'MFNETSOURCE_MAXBUFFERTIMEMS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99d0bf07da8b931ee5487715a4b4430e5ed4384142fc69678a075275d9c7757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243430"
---
# <a name="mfnetsource_maxbuffertimems-property"></a>MFNETSOURCE \_ MAXBUFFERTIMEMS 屬性

網路來源緩衝的最大資料量（以毫秒為單位）。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**DWORD** (儲存為 **LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ MAXBUFFERTIMEMS** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

這個屬性的預設值為40000毫秒。

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

 

 




