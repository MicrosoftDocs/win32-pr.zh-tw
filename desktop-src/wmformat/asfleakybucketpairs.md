---
title: ASFLeakyBucketPairs
description: ASFLeakyBucketPairs 屬性是選擇性屬性，可描述變數位元速率檔案的緩衝需求。
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs windows Media 格式
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965825"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

**ASFLeakyBucketPairs** 屬性是選擇性屬性，可描述變數位元速率檔案的緩衝需求。

## <a name="global-constant"></a>全域常數

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 二進位**

## <a name="remarks"></a>備註

這個屬性的格式如下：

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

其中 *wReserved* 必須等於零，而 *bucket* 是 [**WM \_ 有漏洞 \_ bucket \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) 組結構的陣列。 陣列必須包含至少兩個專案，但可以較大。 讀取器物件會使用此屬性來判斷播放前要緩衝的內容數量。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




