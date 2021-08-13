---
description: '\#網路來源用於記錄的 &0034; c-hostexe&\# 0034; 欄位的值。'
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: 'MFNETSOURCE_HOSTEXE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dbde4b4b445e88a0cb6e7ebe45b8b88f386c208854057f209d9c36b7e0024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463648"
---
# <a name="mfnetsource_hostexe-property"></a>MFNETSOURCE \_ HOSTEXE 屬性

網路來源用來記錄的 "c-hostexe" 欄位值。 應用程式可以將此屬性設定為主應用程式的名稱。 例如，如果應用程式是裝載在網頁中，則此值可能是 "iexplore.exe"。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

寬字元字串 (**WCHAR** \*) 

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>備註

常數 **MFNETSOURCE \_ HOSTEXE** 會定義此屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。

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

 

 




