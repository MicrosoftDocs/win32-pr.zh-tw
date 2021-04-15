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
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372942"
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

 

 




