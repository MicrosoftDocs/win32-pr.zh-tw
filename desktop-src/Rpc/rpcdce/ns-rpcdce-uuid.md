---
title: UUID
description: 提供物件的唯一指定，例如介面、管理員進入點向量或用戶端物件。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092443"
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