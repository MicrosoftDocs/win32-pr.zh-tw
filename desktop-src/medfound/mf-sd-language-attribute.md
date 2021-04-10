---
description: 指定資料流程的語言。
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: 'MF_SD_LANGUAGE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194284"
---
# <a name="mf_sd_language-attribute"></a>MF \_ SD \_ LANGUAGE 屬性

指定資料流程的語言。

## <a name="data-type"></a>資料類型

寬字元字串

## <a name="remarks"></a>備註

這個屬性的值是符合 RFC 1766 規範的語言標記。 這個屬性會套用至資料流程描述項。

如果資料流程具有指定的語言，則媒體來源 (或任何建立資料流程描述項的物件) 可以設定這個屬性。 應用程式可以查詢此屬性來取得語言。 如果未設定屬性，則資料流程沒有指定的語言。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[資料流程描述元屬性](stream-descriptor-attributes.md)
</dt> </dl>

 

 




