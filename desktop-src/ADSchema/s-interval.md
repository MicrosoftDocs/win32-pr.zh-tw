---
title: 間隔語法
description: 表示時間間隔值。
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- 間隔語法 AD 架構
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385318"
---
# <a name="interval-syntax"></a>間隔語法

表示時間間隔值。 實際的時間單位取決於使用此語法的屬性。 這個語法與 [**LargeInteger**](s-largeinteger.md) 語法完全相同，但最高值和最低值都是不帶正負號的整數。



| 進入 | 值 |
|--------------|------------------------------------------------------------------------------------|
| 名稱         | 間隔                                                                           |
| 語法識別碼    | 2.5.5.16                                                                           |
| OM 識別碼        | 65                                                                                 |
| MAPI 類型    | \-                                                                                 |
| ADS 類型     | ADSTYPE \_ 大型 \_ 整數                                                            |
| Variant 類型 | VT \_ 分派                                                                       |
| SDS 類型     | 可以轉換成 [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)的 COM 物件。 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[**LargeInteger**](s-largeinteger.md)
</dt> </dl>

 

 
