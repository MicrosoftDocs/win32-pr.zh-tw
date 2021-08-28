---
title: OP_PACKAGE
description: OP_PACKAGE IDL 定義
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81fdc237b731489f7ac501a4e053e62d744b0fdef77c5b630cd478dede5aeda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911488"
---
# <a name="op_package-structure"></a>OP_PACKAGE 結構

包含包含序列化 OP_PACKAGE_COLLECTION 的結構。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a>成員

### <a name="encryptiontype"></a>EncryptionType

保留供日後使用，且必須設定為 GUID_Null。

### <a name="encryptioncontext"></a>EncryptionCoNtext

保留供日後使用，且必須設定為全部為零。

### <a name="wrappedpartcollection"></a>WrappedPartCollection

包含序列化 OP_PACKAGE_COLLECTION 結構的 OP_BLOB 結構。

### <a name="cbdecryptedpartcollection"></a>cbDecryptedPartCollection

保留供日後使用，且必須設定為零。

### <a name="extension"></a>延伸模組

保留供日後使用，且必須設定為全部為零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ BLOB**](odj-op_blob.md)

[**OP \_ 套件 \_ 集合**](odj-op_package_collection.md)
