---
description: 字串陣列，其中包含要傳送至記錄伺服器的參數。
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: 'MFNETSOURCE_LOGPARAMS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba557c4fb0bf77693669e8cb46af269ec3a4f2ed72c536e4bdab53a0778dc038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113518"
---
# <a name="mfnetsource_logparams-property"></a>MFNETSOURCE \_ LOGPARAMS 屬性

字串陣列，其中包含要傳送至記錄伺服器的參數。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**WCHAR\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>備註

**MFNETSOURCE \_ LOGPARAMS** 常數會定義屬性索引鍵的 GUID。  (PID) 的屬性識別碼為零。 若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

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
</dt> </dl>

 

 




