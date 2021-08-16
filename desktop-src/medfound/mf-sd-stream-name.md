---
description: 包含資料流程的名稱。
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: 'MF_SD_STREAM_NAME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312ca788b03c3bef075c2c51d06df921d258e7372c091c5ccb43ec248444fcfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474052"
---
# <a name="mf_sd_stream_name-attribute"></a>MF \_ SD \_ STREAM \_ NAME 屬性

包含資料流程的名稱。

## <a name="data-type"></a>資料類型

**WCHAR\***

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="applies-to"></a>適用於

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>備註

如果 AVI 檔案包含 ' strn ' 區塊，則 AVI 媒體來源會設定此屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[資料流程描述元屬性](stream-descriptor-attributes.md)
</dt> </dl>

 

 




