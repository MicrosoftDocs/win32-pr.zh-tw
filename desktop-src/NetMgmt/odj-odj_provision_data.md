---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA IDL 定義
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 02762a80be9bd60b7f9c8648c9bfb848f3d76184f249567c9e9522189692e0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064348"
---
# <a name="odj_provision_data-structure"></a>ODJ_PROVISION_DATA 結構

指定離線網域加入 api 所使用的最外層序列化結構。

## <a name="syntax"></a>語法

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a>成員

### <a name="ulversion"></a>ulVersion

這必須設定為1。

### <a name="ulcblobs"></a>ulcBlobs

這必須設定為 pBlobs 陣列中的元素數目。

### <a name="pblobs"></a>pBlobs

指向 ODJ_BLOB 結構的陣列。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**ODJ \_ BLOB**](odj-odj_blob.md)


