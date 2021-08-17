---
description: 指定 ASF 媒體來源是否使用近似搜尋。
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: 'MFPKEY_ASFMediaSource_ApproxSeek 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f68dedbf2b008870021e620029a039c21465d4bb45a23428225d7c88fae6583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874332"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>MFPKEY \_ ASFMediaSource \_ ApproxSeek 屬性

指定 ASF 媒體來源是否使用近似搜尋。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>備註

應用程式可以使用這個屬性來設定 ASF 媒體來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

ASF 媒體來源處理搜尋的方式如下：

-   如果這個屬性的值為 **VARIANT \_ TRUE**，則媒體來源會使用近似的搜尋，其精確度較低，但比確切搜尋更快。
-   如果此值為 **VARIANT \_ FALSE** ，且 ASF 檔案有索引，則媒體來源會使用精確的搜尋。
-   如果 ASF 檔案不包含索引，除非 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) 屬性設定為 **VARIANT \_ TRUE**，否則媒體來源會使用 approxmate 搜尋。
-   如果 ASF 檔案未包含索引，且 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) 屬性為 **VARIANT \_ TRUE**，則媒體來源會使用反復搜尋。 反復搜尋的精確度較高，但比近似搜尋 (更慢，但通常不如搜尋) 精確。
    > [!Note]  
    > 需要 Windows 7。

     

這個屬性的預設值為 **VARIANT \_ FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




