---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING IDL 定義
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "106966276"
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
