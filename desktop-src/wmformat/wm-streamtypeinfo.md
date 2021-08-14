---
title: WM/StreamTypeInfo
description: WM/StreamTypeInfo 屬性包含 ASF 檔案中指定之資料流程的設定資訊。
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- WM/StreamTypeInfo windows Media 格式
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb40926d5ecba3aea2c7f2db64850152c66a25861d4422fddf04670c76d8148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698270"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

**WM/StreamTypeInfo** 屬性包含 ASF 檔案中指定之資料流程的設定資訊。

## <a name="global-constant"></a>全域常數

g \_ wszWMStreamTypeInfo

## <a name="data-type"></a>資料類型

[**WM \_資料流程 \_ 類型 \_ 資訊**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT \_ 類型 \_ BINARY**) 

## <a name="remarks"></a>備註

這個屬性會套用到特定的資料流程。 您無法抓取資料流程0的這個屬性。

這個屬性是唯讀的。

您可以使用 [中繼資料編輯器] 物件來存取 **WM/StreamTypeInfo** 。 這是存取串流設定資訊的唯一方法，不需要使用 reader 物件 (或同步讀取器物件) 來開啟檔案。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




