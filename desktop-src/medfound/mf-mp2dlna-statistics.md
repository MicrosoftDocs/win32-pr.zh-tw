---
description: 取得數位客廳網路聯盟 (DLNA) 媒體接收器的統計資料。
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: 'MF_MP2DLNA_STATISTICS 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512832"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>MF \_ MP2DLNA \_ 統計資料屬性

取得數位客廳網路聯盟 (DLNA) 媒體接收器的統計資料。

## <a name="data-type"></a>資料類型

**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** 儲存為 **位元組 \[ \]**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

## <a name="remarks"></a>備註

在串流處理期間，DLNA 媒體接收器會使用 MPEG-2 資料流程的編碼和多工處理相關統計資料來更新此屬性。 應用程式可以隨時查詢這個屬性，以取得最新的值。

在 DLNA 媒體接收器上設定此屬性沒有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmp2dlna。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




