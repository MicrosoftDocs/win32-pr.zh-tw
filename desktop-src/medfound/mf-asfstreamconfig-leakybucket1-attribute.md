---
description: 設定平均 &\# 0034; 有漏洞 bucket&\# 0034; 參數 (請參閱備註) ，以編碼 Windows Media 檔案。 使用 IMFASFStreamConfig 介面設定這個屬性。
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: 'MF_ASFSTREAMCONFIG_LEAKYBUCKET1 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982325"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a>MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1 屬性

設定「有漏洞值區」的平均參數 (查看針對 Windows Media 檔案進行編碼的備註) 。 使用 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面設定這個屬性。

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

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




