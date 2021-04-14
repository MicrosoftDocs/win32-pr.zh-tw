---
title: OP_BLOB
description: OP_BLOB IDL 定義
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383177"
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
