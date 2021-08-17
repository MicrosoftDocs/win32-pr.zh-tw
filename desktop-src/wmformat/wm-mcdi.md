---
title: WM/MCDI
description: WM/MCDI 屬性包含音樂 CD 識別碼。 這是 CD 中目錄的二進位傾印，可用來唯一識別 CD。
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- WM/MCDI windows Media 格式
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccf4a081141c1902fe93680937a3196e015e6690acf76d69f3a3d8a016c092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963747"
---
# <a name="wmmcdi"></a>WM/MCDI

**WM/MCDI** 屬性包含音樂 CD 識別碼。 這是 CD 中目錄的二進位傾印，可用來唯一識別 CD。

## <a name="global-constant"></a>全域常數

g \_ wszWMMCDI

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 二進位**

## <a name="remarks"></a>備註

這個屬性與 ID3 框架 MCDI 相容。 MCDI 框架的 ID3 規格需要每個檔案只有一個這類畫面格，而且有一個有效的 TRCK 框架存在。 中繼資料編輯器不會執行這些規則的任何驗證。 此外，WM/MCDI 的大小不會限制為804個位元組，如同 MCDI ID3 框架一樣。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




