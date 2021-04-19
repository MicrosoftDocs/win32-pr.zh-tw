---
description: 在建立時將 IMFMediaEngineNeedKeyNotify 傳遞給媒體引擎的屬性。
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106993787"
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
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




