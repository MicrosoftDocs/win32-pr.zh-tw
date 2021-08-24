---
description: 使用 Advanced Systems 格式之二進位資料流程的特定類型資料 (ASF) 檔。
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: 'MF_MT_ARBITRARY_HEADER 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d824aad4f76947786f991807d2f7b301703e3e356d2d1cfb416aa634d49f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826518"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>MF \_ MT \_ 任意 \_ 標頭屬性

使用 Advanced Systems 格式之二進位資料流程的特定類型資料 (ASF) 檔。

## <a name="data-type"></a>資料類型

**[**MT \_任意 \_**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** 儲存為 **位元組 \[ \]** 的標頭

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="remarks"></a>備註

ASF 檔案可以包含具有二進位資料的資料流程。 \_ \_ 媒體類型中的 MF MT 任意 \_ 標頭屬性包含描述資料流程的 [**MT \_ 任意 \_ 標頭**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)結構。

除了 MF \_ MT \_ 任意 \_ 標頭屬性之外，ASF 二進位資料流程的媒體類型還包含下列屬性：



| 屬性                                                 | 描述                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) | 屬性的值為 **MFMediaType \_ Binary**。 |
| [MF \_ MT \_ 任意 \_ 格式](mf-mt-arbitrary-format.md)   | 包含其他格式資料。                       |



 

> [!Note]  
> 在 Windows 媒體格式 SDK 中，二進位資料流程稱為 *任意資料流程* 或 *任意* 資料流程。

 

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




