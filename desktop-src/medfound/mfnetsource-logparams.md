---
description: 字串陣列，其中包含要傳送至記錄伺服器的參數。
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: 'MFNETSOURCE_LOGPARAMS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943780"
---
# <a name="mfnetsource_logparams-property"></a>MFNETSOURCE \_ LOGPARAMS 屬性

字串陣列，其中包含要傳送至記錄伺服器的參數。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**WCHAR \** _

VT \_ LPWSTR

_ *pwszVal**



## <a name="remarks"></a>備註

**MFNETSOURCE \_ LOGPARAMS** 常數會定義屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。 若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

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

 

 




