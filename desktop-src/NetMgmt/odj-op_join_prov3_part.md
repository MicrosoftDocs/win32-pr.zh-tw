---
title: OP_JOINPROV3_PART
description: OP_JOINPROV3_PART IDL 定義
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383169"
---
# <a name="op_joinprov3_part-structure"></a>OP_JOINPROV3_PART 結構

包含用來設定加入網域之用戶端的其他資訊。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>成員

### <a name="rid"></a>擺脫

必須設定為電腦帳戶 SID 的相對識別碼

### <a name="lpsid"></a>lpSid

必須設定為字串格式之電腦帳戶的 SID。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)
