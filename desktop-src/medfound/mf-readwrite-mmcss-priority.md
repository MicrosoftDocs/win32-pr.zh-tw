---
description: 設定來源讀取器或接收寫入器的基底線程優先順序。
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: 'MF_READWRITE_MMCSS_PRIORITY 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027427"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>MF \_ READWRITE \_ MMCSS \_ PRIORITY 屬性

設定來源讀取器或接收寫入器的基底線程優先順序。

## <a name="data-type"></a>資料類型

以 **UINT32** 儲存的 **INT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

當您建立 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)的實例時，可選擇性地設定這個屬性。 如果您設定此屬性，也請設定 [MF \_ READWRITE \_ MMCSS \_ 類別](mf-readwrite-mmcss-class.md) 屬性。 否則，會忽略這個屬性。

當來源讀取器或接收寫入器向 [多媒體類別](../procthread/multimedia-class-scheduler-service.md)排程器服務註冊執行緒時，這個屬性的值會指定基底線程優先順序。 如果未設定此屬性，則預設值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
