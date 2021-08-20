---
title: OP_PACKAGE_PART_COLLECTION
description: OP_PACKAGE_PART_COLLECTION IDL 定義
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 26a664bc05cc076ac6e4fb945c5381fd5d7075ec6653c807230cc97a7db135f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983419"
---
# <a name="op_package_part_collection-structure"></a>OP_PACKAGE_PART_COLLECTION 結構

指定包含 OP_PACKAGE_PART 結構陣列的結構。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a>成員

### <a name="cparts"></a>cParts

包含 pParts 中的元素數目。

### <a name="pparts"></a>pParts

包含 OP_PACKAGE_PART 結構的陣列。

### <a name="extension"></a>延伸模組

保留供日後使用，且必須設定為全部為零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ 套件 \_ 部分**](odj-op_package_part.md)

[**OP \_ BLOB**](odj-op_blob.md)

