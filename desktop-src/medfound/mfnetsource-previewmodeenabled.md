---
description: 啟用或停用預覽模式，此模式可讓應用程式覆寫初始的緩衝邏輯。
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: 'MFNETSOURCE_PREVIEWMODEENABLED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996847"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>MFNETSOURCE \_ PREVIEWMODEENABLED 屬性

啟用或停用預覽模式，此模式可讓應用程式覆寫初始的緩衝邏輯。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**Bool**

VT \_ BOOL

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PREVIEWMODEENABLED** 會定義屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。 這個屬性是在網路來源上設定的，方法是將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




