---
description: 在建立時將 IMFMediaEngineNeedKeyNotify 傳遞給媒體引擎的屬性。
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bec8dd3b802d9fc378d43648ad1d29dd30b6573881a044cc9f0d3aba2015cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956308"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a>MF \_ 媒體 \_ 引擎 \_ NEEDKEY \_ 回呼屬性

在建立時將 [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) 傳遞給媒體引擎的屬性。

## <a name="data-type"></a>資料類型

**IMFMediaEngineNeedKeyNotify \* *_ 儲存為 _* IUnknown\***

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

這個屬性的值是 [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) 介面的指標，該介面是由應用程式所執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




