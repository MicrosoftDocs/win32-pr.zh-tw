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
# <a name="uuid-structure"></a><span data-ttu-id="979f2-103">UUID 結構</span><span class="sxs-lookup"><span data-stu-id="979f2-103">UUID structure</span></span>

<span data-ttu-id="979f2-104">**Uuid** 結構會定義 (UUID) 的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="979f2-104">The **UUID** structure defines a Universally Unique Identifier (UUID).</span></span> <span data-ttu-id="979f2-105">**UUID** 提供物件的唯一指定，例如介面、管理員進入點向量或用戶端物件。</span><span class="sxs-lookup"><span data-stu-id="979f2-105">A **UUID** provides a unique designation of an object such as an interface, a manager entry-point vector, or a client object.</span></span>

<span data-ttu-id="979f2-106">**UUID** 結構是 `typedef` [GUID](/windows/win32/api/guiddef/ns-guiddef-guid)結構的同義字。</span><span class="sxs-lookup"><span data-stu-id="979f2-106">The **UUID** structure is a `typedef`'d synonym for the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="979f2-107">語法</span><span class="sxs-lookup"><span data-stu-id="979f2-107">Syntax</span></span>

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a><span data-ttu-id="979f2-108">備註</span><span class="sxs-lookup"><span data-stu-id="979f2-108">Remarks</span></span>

<span data-ttu-id="979f2-109">RPC 執行時間程式庫會使用 **UUID** 來檢查用戶端與伺服器之間的相容性，以及在介面的多個介面中進行選取。</span><span class="sxs-lookup"><span data-stu-id="979f2-109">The RPC run-time libraries use **UUID** s to check for compatibility between clients and servers, and to select among multiple implementations of an interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="979f2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="979f2-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="979f2-111">**標頭**</span><span class="sxs-lookup"><span data-stu-id="979f2-111">**Header**</span></span> | <span data-ttu-id="979f2-112">定義于 rpcdce 中;包含 rpc。h</span><span class="sxs-lookup"><span data-stu-id="979f2-112">Defined in rpcdce.h; include rpc.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="979f2-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="979f2-113">See also</span></span>

<span data-ttu-id="979f2-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
[UUID \_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span><span class="sxs-lookup"><span data-stu-id="979f2-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)
[UUID\_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span></span>