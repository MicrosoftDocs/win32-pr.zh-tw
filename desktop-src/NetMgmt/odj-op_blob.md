---
title: OP_BLOB
description: OP_BLOB IDL 定義
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 757df1549d1bdb0a9a87ee22373a1903a034a1e267d087d51dac46bb6bc5a762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796888"
---
# <a name="op_blob-structure"></a>OP_BLOB 結構

包含不透明的位元組緩衝區。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>成員

### <a name="cbblob"></a>cbBlob

指定 pBlob 的大小（以位元組為單位）。

### <a name="pblob"></a>pBlob

指向位元組緩衝區。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)
