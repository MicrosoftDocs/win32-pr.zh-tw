---
title: OP_PACKAGE_PART_COLLECTION
description: OP_PACKAGE_PART_COLLECTION IDL 定義
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104024281"
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

### <a name="extension"></a>分機

保留供日後使用，且必須設定為全部為零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ 套件 \_ 部分**](odj-op_package_part.md)

[**OP \_ BLOB**](odj-op_blob.md)

