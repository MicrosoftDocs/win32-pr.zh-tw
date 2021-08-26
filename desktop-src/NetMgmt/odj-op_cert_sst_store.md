---
title: OP_CERT_SST_STORE
description: OP_CERT_SST_STORE IDL 定義
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 4104635ea845394251f28eea48a2b3c67063826f98dd4da71a8f9adda8fd14a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911548"
---
# <a name="op_cert_sst_store-structure"></a>OP_CERT_SST_STORE 結構

包含序列化的憑證存放區。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a>成員

### <a name="storelocation"></a>StoreLocation

包含 [**系統存放區位置**](../seccrypto/system-store-locations.md)中憑證存放區的識別碼。

### <a name="pstorename"></a>pStoreName

包含存放區的名稱。

### <a name="cbsst"></a>cbSst

包含 pSst 的大小（以位元組為單位）。

### <a name="psst"></a>pSst

包含序列化的憑證存放區 (請參閱 [**RFC 7292**](https://tools.ietf.org/html/rfc7292)) 。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)