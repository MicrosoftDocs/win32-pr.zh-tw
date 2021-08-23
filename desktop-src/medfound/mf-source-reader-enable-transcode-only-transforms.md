---
description: 可讓來源讀取器使用媒體基礎轉換， (MFTs) 已針對轉碼進行優化。
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: 'MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc5362c93138ef301ac65ace799ad64d59ac9110af349822e0efa98d410686e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605015"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 轉碼 \_ 僅限 \_ 轉換屬性

可讓 [來源讀取器](source-reader.md) 使用媒體基礎轉換， (MFTs) 已針對轉碼進行優化。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

某些 MFTs （特別是在不同的解碼器）會針對轉碼進行優化，而不是播放。 根據預設，來源讀取器不會載入這類轉換。 如果您想要在來源讀取器中使用轉碼 MFTs，請將此屬性設定為 **TRUE** 。

應用程式可能會設定這個屬性，如果它不會即時處理轉碼或類似案例) 的資料 (。 否則，若為即時播放，請使用預設行為。

就內部而言，此屬性會讓來源讀取器在呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)時，**只包含 MFT \_ 列舉 \_ 旗標 \_ 轉碼 \_** 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> </dl>

 

 




