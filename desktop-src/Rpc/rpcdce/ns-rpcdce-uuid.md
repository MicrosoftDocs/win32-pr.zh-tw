---
title: UUID
description: 提供物件的唯一指定，例如介面、管理員進入點向量或用戶端物件。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 31ff8eb22a234020e0da5b5ebb5799d5ddb0c8d1dca7bc094394f79a5ceb0c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925945"
---
# <a name="uuid-structure"></a>UUID 結構

**Uuid** 結構會定義 (UUID) 的通用唯一識別碼。 **UUID** 提供物件的唯一指定，例如介面、管理員進入點向量或用戶端物件。

**UUID** 結構是 `typedef` [GUID](/windows/win32/api/guiddef/ns-guiddef-guid)結構的同義字。

## <a name="syntax"></a>語法

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>備註

RPC 執行時間程式庫會使用 **UUID** 來檢查用戶端與伺服器之間的相容性，以及在介面的多個介面中進行選取。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | 定義于 rpcdce 中;包含 rpc。h |

## <a name="see-also"></a>另請參閱

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
[UUID \_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)