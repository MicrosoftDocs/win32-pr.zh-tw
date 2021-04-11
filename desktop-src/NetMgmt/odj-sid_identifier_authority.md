---
title: SID_IDENTIFIER_AUTHORITY
description: SID_IDENTIFIER_AUTHORITY IDL 定義
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104093483"
---
# <a name="sid_identifier_authority-structure"></a>SID_IDENTIFIER_AUTHORITY 結構

包含 SID 識別碼授權單位。

## <a name="syntax"></a>語法

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>成員

### <a name="value"></a>值

必須設定為 SID 識別碼授權單位的六個位元組。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)