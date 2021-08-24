---
title: " (一般化時間) 語法的字串"
description: 由 ASN. 1 標準定義的時間字串格式。 | (一般化時間) 語法的字串
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- 字串 (一般化時間) 語法 AD 架構
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bf7d965b03b75f4186b807098a5262c402d0c19104a4c09357958b38a77a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580208"
---
# <a name="stringgeneralized-time-syntax"></a> (一般化時間) 語法的字串

由 ASN. 1 標準定義的時間字串格式。 使用此語法，以 Generalized-Time 格式儲存時間值。

Generalized-Time 語法的格式為 "YYYYMMDDHHMMSS.FFFFFF. 0Z"。 可接受值的範例是「20010928060000.0 Z」。 "Z" 表示沒有時間差異。 Active Directory 將日期/時間儲存為格林威治標準時間 (GMT) 。 如果未指定時間差異，則預設值為 GMT。

如果時間是在 GMT 以外的時區中指定，則時區與 gmt 之間的差異會附加至字串，而不是 "yyyymmddhhmmss.ffffff. 0 HHMM" 格式的 "Z" \[ +/- \] 。 可接受值的範例是 "20010928060000.0 + 0200"。 差異是以公式： GMT = Local + 差異為基礎。

如需詳細資訊，請參閱 ISO 8601 和 X680。



| 進入 | 值 |
|--------------|----------------------------------------------------------------------------|
| 名稱         | String(Generalized-Time)                                                   |
| 語法識別碼    | 2.5.5.11                                                                   |
| OM 識別碼        | 24                                                                         |
| MAPI 類型    | SYSTIME                                                                    |
| ADS 類型     | ADSTYPE \_ UTC \_ 時間                                                         |
| Variant 類型 | VT \_ 日期                                                                   |
| SDS 類型     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
