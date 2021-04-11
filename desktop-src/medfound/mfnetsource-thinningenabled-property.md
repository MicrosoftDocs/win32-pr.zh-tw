---
description: 指定是否啟用網路來源的資料流程切換。
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: 'MFNETSOURCE_THINNINGENABLED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936555"
---
# <a name="mfnetsource_thinningenabled-property"></a>MFNETSOURCE \_ THINNINGENABLED 屬性

指定是否啟用網路來源的資料流程切換。 串流切換可讓媒體伺服器根據可用的頻寬，以多個位元速率 (MBR) 檔來變更資料流程。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

布林 (**LONG**) 

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ THINNINGENABLED** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

這個屬性的預設值為 **TRUE**。

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

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




