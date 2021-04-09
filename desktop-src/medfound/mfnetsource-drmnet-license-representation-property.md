---
description: 儲存位元組陣列，表示與位元組資料流程相關聯的 DRM 授權。
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: 'MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691240"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>MFNETSOURCE \_ DRMNET \_ 授權 \_ 表示屬性

儲存位元組陣列，表示與位元組資料流程相關聯的 DRM 授權。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

 (**BLOB** 的位元組陣列) 

VT \_ BLOB

**blob**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ DRMNET \_ 授權 \_ 表示** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

這是唯讀的屬性。 若要從網路位元組資料流程取得屬性值，請呼叫 **IPropertyStore：： GetValue** ，並在 *key* 參數中傳遞 **PROPERTYKEY** 結構。 **PROPERTYKEY** 的 **fmtid** 成員必須設定為屬性 GUID。

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

 

 




