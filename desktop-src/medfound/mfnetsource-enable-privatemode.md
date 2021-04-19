---
description: 在網路來源中啟用私用下載模式。
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: 'MFNETSOURCE_ENABLE_PRI加值稅EMODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971453"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MFNETSOURCE \_ ENABLE \_ PRI加值稅EMODE 屬性

在網路來源中啟用私用下載模式。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**Bool**

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

如果這個屬性為 **TRUE**，則會在會話結束時清除快取。

**MFNETSOURCE \_ CLIENTGUID** 常數會定義屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。 若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




