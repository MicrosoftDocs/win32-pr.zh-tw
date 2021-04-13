---
title: 查找
description: 可搜尋的屬性是檔案層級屬性，可指定應用程式是否可以搜尋內容中的點。
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- 能搜尋的 windows 媒體格式
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314499"
---
# <a name="seekable"></a>查找

可搜尋的屬性是檔案層級 **屬性，可** 指定應用程式是否可以搜尋內容中的點。

## <a name="global-constant"></a>全域常數

g \_ wszWMSeekable

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

這是程式碼屬性。

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。

檔案的這個屬性值可能會根據公開用來抓取 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 或 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面的物件而有所不同。 這是因為「讀取器」物件 (同步和非同步) 執行比「中繼資料編輯器」物件更完整的檢查，以確定您是否可以搜尋檔案中的某個點。 讀取器物件所傳回的可 **搜尋屬性值** 比較精確。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




