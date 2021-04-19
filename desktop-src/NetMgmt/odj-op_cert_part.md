---
title: OP_CERT_PART
description: OP_CERT_PART IDL 定義
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "106966482"
---
# <a name="op_cert_part-structure"></a>OP_CERT_PART 結構

包含已序列化的 PFX 和憑證存放區。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a>成員

### <a name="cpfxstores"></a>cPfxStores

包含 pPfxStores 中的元素數目。

### <a name="ppfxstores"></a>pPfxStores

包含 OP_CERT_PFX_STORE 結構的陣列。

### <a name="csststores"></a>cSstStores

包含 pSstStores 中的元素數目。

### <a name="psststores"></a>pSstStores

包含 OP_CERT_SST_STORE 結構的陣列。

### <a name="extension"></a>分機

保留供日後使用，且必須包含所有的零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ CERT \_ PFX \_ 存放區**](odj-op_cert_pfx_store.md)

[**OP \_ CERT \_ .SST \_ STORE**](odj-op_cert_sst_store.md)

[**OP \_ BLOB**](odj-op_blob.md)

