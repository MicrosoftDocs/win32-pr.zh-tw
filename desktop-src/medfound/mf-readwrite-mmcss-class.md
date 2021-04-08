---
description: 為來源讀取器或接收寫入器指定多媒體類別排程器服務 (MMCSS) 類別。
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: 'MF_READWRITE_MMCSS_CLASS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694692"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>MF \_ READWRITE \_ MMCSS \_ 類別屬性

為來源讀取器或接收寫入器指定 [多媒體類別](../procthread/multimedia-class-scheduler-service.md) 排程器服務 (MMCSS) 類別。

## <a name="data-type"></a>資料類型

**LPWSTR**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="remarks"></a>備註

當您建立 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)的實例時，可選擇性地設定這個屬性。 屬性的值必須是有效的 MMCSS 類別名稱。

如果設定這個屬性，來源讀取器或接收寫入器會使用指定的 MMCSS 類別來註冊其所有線程。 MMCSS 可確保來源讀取器或接收寫入器中的資料處理優先順序高於其他系統工作。

若要指定基本優先權，請設定 [ [MF \_ READWRITE \_ MMCSS \_ priority](mf-readwrite-mmcss-priority.md) ] 屬性。 如果未設定該屬性，則基本優先權為零。

針對音訊處理執行緒，如果 set) 覆寫此屬性，則 (的 [MF \_ READWRITE \_ MMCSS \_ 類別 \_ 音訊](mf-readwrite-mmcss-class-audio.md) 屬性。

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

 

 
