---
description: '\#網路來源用於記錄的 &0034; c-hostexever&\# 0034; 欄位的值。'
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: 'MFNETSOURCE_HOSTVERSION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5f78a277de4fc5b0609be31f21f684357806dbb8609657a930cdc4816b1e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243458"
---
# <a name="mfnetsource_hostversion-property"></a>MFNETSOURCE \_ HOSTVERSION 屬性

網路來源用來記錄的 "c-hostexever" 欄位值。 應用程式可以將此屬性設定為主應用程式的版本號碼。 主應用程式是 hostexe 欄位所識別的 .exe 檔案。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ HOSTVERSION** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

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

 

 




