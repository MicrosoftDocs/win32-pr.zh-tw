---
title: ODJ_BLOB
description: ODJ_BLOB IDL 定義
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104463889"
---
# <a name="odj_blob-structure"></a>ODJ_BLOB 結構

指定包含序列化 ODJ_WIN7BLOB 結構或序列化 OP_PACKAGE 結構的結構。

## <a name="syntax"></a>語法

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>成員

### <a name="ulodjformat"></a>ulODJFormat

指定結構的邏輯版本，且必須設定為下列其中一個值：

|值|意義|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001) |PBlob 中包含的位元組必須包含序列化的 ODJ_WIN7_BLOB 結構。|
|ODJ_WIN8_FORMAT (0x00000002) |PBlob 中包含的位元組必須包含序列化的 OP_PACKAGE 結構。|

### <a name="cbblob"></a>cbBlob

這必須設定為 pBlob 陣列中的位元組數目。

### <a name="pblob"></a>pBlob

指向包含序列化結構的位元組緩衝區（如上述 ulODJFormat 所指定）。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

