---
description: 設定尖峰 &\# 0034; 有漏洞 bucket&\# 0034; 參數 (請參閱備註) ，以編碼 Windows Media 檔案。 這些參數會用於尖峰位元速率。 使用 IMFASFStreamConfig 介面設定這個屬性。
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: 'MF_ASFSTREAMCONFIG_LEAKYBUCKET2 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990327"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2 屬性

設定尖峰 "有漏洞 bucket" 參數 (請參閱備註) 來編碼 Windows Media 檔案。 這些參數會用於尖峰位元速率。 使用 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面設定這個屬性。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

這個屬性的值是三個 **DWORD** 的陣列，順序如下：

-   位元速率，以每秒位數為單位。
-   緩衝區視窗（以毫秒為單位）。
-   初始緩衝區飽和度（以位元組為單位）。

如需有關有漏洞 bucket 概念的詳細資訊，請參閱 Windows Media Format SDK 檔中 [的有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md) 主題。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF 屬性](asf-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




