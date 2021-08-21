---
description: '\#網路來源用於記錄的 &0034; c-playerversion&\# 0034; 欄位的值。'
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: 'MFNETSOURCE_PLAYERVERSION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71828db44eca7c4318dbdb11e7934871911b06dbc4547f83723a9944f139ae26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738967"
---
# <a name="mfnetsource_playerversion-property"></a>MFNETSOURCE \_ PLAYERVERSION 屬性

網路來源用來記錄的 "c-playerversion" 欄位值。 應用程式可以將此屬性設定為應用程式的版本號碼。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ PLAYERVERSION** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱 [來源解析程式](source-resolver.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端記錄](client-logging.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




