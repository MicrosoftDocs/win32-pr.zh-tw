---
description: 指定是否在網路來源中啟用媒體串流廣播 (MSB) 多播通訊協定。
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: 'MFNETSOURCE_ENABLE_MSB 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1054b4a94bf966457ddeccc606fbd2fd2c8a1d5b3978b830b5e3c48f0f93b5ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243815"
---
# <a name="mfnetsource_enable_msb-property"></a>MFNETSOURCE \_ ENABLE \_ MSB 屬性

指定是否在網路來源中啟用媒體串流廣播 (MSB) 多播通訊協定。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ ENABLE \_ MSB** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

應用程式可以使用這個屬性來設定網路來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> <dt>

[支援的通訊協定](supported-protocols.md)
</dt> </dl>

 

 




