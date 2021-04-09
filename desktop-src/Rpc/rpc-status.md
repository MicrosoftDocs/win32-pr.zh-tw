---
title: 'RPC_STATUS (Rpcdce) '
description: 資料類型 RPC \_ 狀態代表平臺特定的狀態碼類型。
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025062"
---
# <a name="rpc_status"></a><span data-ttu-id="ae720-105">RPC \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="ae720-105">RPC\_STATUS</span></span>

<span data-ttu-id="ae720-106">資料類型 **RPC \_ 狀態** 代表平臺特定的狀態碼類型。</span><span class="sxs-lookup"><span data-stu-id="ae720-106">The data type **RPC\_STATUS** represents a platform-specific status code type.</span></span>


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a><span data-ttu-id="ae720-107">備註</span><span class="sxs-lookup"><span data-stu-id="ae720-107">Remarks</span></span>

<span data-ttu-id="ae720-108">**Rpc \_ 狀態** 類型是由大部分 rpc 函式傳回，而且屬於 [**rpc \_ 物件 \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)函數類型定義的一部分。</span><span class="sxs-lookup"><span data-stu-id="ae720-108">The **RPC\_STATUS** type is returned by most RPC functions and is part of the [**RPC\_OBJECT\_INQ\_FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) function type definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae720-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae720-109">Requirements</span></span>



| <span data-ttu-id="ae720-110">需求</span><span class="sxs-lookup"><span data-stu-id="ae720-110">Requirement</span></span> | <span data-ttu-id="ae720-111">值</span><span class="sxs-lookup"><span data-stu-id="ae720-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae720-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae720-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ae720-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae720-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ae720-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae720-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ae720-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae720-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ae720-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ae720-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae720-117"><dt>Rpcdce (包含 Rpc) </dt></span><span class="sxs-lookup"><span data-stu-id="ae720-117"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae720-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae720-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae720-119">**RPC \_ 物件 \_ INQ \_ FN**</span><span class="sxs-lookup"><span data-stu-id="ae720-119">**RPC\_OBJECT\_INQ\_FN**</span></span>](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





