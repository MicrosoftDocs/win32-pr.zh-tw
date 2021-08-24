---
description: 指定多媒體類別排程器服務 (MMCSS 來源讀取器或接收寫入器中音訊處理執行緒的) 類別。
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: 'MF_READWRITE_MMCSS_CLASS_AUDIO 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f416c22619c0777ef244e6566328154bf7a7336587fc73a3f29626fcdaa1c462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119345278"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>MF \_ READWRITE \_ MMCSS \_ 類別 \_ 音訊屬性

指定 [多媒體類別](../procthread/multimedia-class-scheduler-service.md) 排程器服務 (MMCSS 來源讀取器或接收寫入器中音訊處理執行緒的) 類別。

## <a name="data-type"></a>資料類型

**LPWSTR**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="remarks"></a>備註

當您建立 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)的實例時，可選擇性地設定這個屬性。 屬性的值必須是有效的 MMCSS 類別名稱。

如果設定這個屬性，來源讀取器或接收寫入器會使用指定的 MMCSS 類別來註冊其音訊處理執行緒。 MMCSS 可確保來源讀取器或接收寫入器中的資料處理優先順序高於其他系統工作。

若要指定音訊執行緒的基本優先權，請設定 [ [MF \_ READWRITE \_ MMCSS \_ priority \_ 音訊](mf-readwrite-mmcss-priority-audio.md) ] 屬性。 如果未設定該屬性，則音訊執行緒的基本優先權為零。

這個屬性會覆寫音訊處理執行緒的 [MF \_ READWRITE \_ MMCSS \_ 類別](mf-readwrite-mmcss-class.md) 屬性。 如果未設定這兩個屬性，則不會向 MCSS 註冊音訊執行緒。

對於大部分的應用程式而言，音訊瑕疵比影片瑕疵更加明顯，因此較不容易接受。 基於這個理由，應用程式通常應該將 MF \_ readwrite \_ MMCSS \_ 類別 \_ 音訊設定為比 [MF \_ readwrite \_ MMCSS \_ 類別](mf-readwrite-mmcss-class.md)更高優先順序的 MMCSS 類別。 這可確保音訊處理的優先順序高於其他工作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
