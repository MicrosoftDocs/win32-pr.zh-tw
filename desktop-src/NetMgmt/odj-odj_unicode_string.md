---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING IDL 定義
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3578c62f110eafd053ed97bbe1f8b5015156d02c4b879ff8111ff13f28dfab33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891237"
---
# <a name="odj_unicode_string-structure"></a>ODJ_UNICODE_STRING 結構

包含 Unicode 字串。

## <a name="syntax"></a>語法

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a>成員

### <a name="length"></a>長度

必須設定為包含字串的緩衝區中的位元組數目，不包括 Null 結束字元。

### <a name="maximumlength"></a>MaximumLength

這必須設定為緩衝區中的總位元組數，不包括 Null 結束字元。

### <a name="buffer"></a>Buffer

必須為 Unicode 字串。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)
