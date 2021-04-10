---
title: 'PROTOCOL_SPECIFIC_DATA 結構 (Rtm) '
description: 通訊協定 \_ 特定的 \_ 資料結構包含特定路由通訊協定專屬資料的保留記憶體。
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA 結構 RAS
- PPROTOCOL_SPECIFIC_DATA 結構指標 RAS
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686080"
---
# <a name="protocol_specific_data-structure"></a><span data-ttu-id="cb543-105">通訊協定 \_ 特定的 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="cb543-105">PROTOCOL\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="cb543-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="cb543-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="cb543-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="cb543-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="cb543-108">**通訊協定 \_ 特定的 \_ 資料** 結構包含特定路由通訊協定專屬資料的保留記憶體。</span><span class="sxs-lookup"><span data-stu-id="cb543-108">The **PROTOCOL\_SPECIFIC\_DATA** structure contains memory reserved for data specific to a particular routing protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb543-109">語法</span><span class="sxs-lookup"><span data-stu-id="cb543-109">Syntax</span></span>


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="cb543-110">成員</span><span class="sxs-lookup"><span data-stu-id="cb543-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb543-111">**PSD \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="cb543-111">**PSD\_Data**</span></span>
</dt> <dd>

<span data-ttu-id="cb543-112">指定 **DWORD** 變數的陣列。</span><span class="sxs-lookup"><span data-stu-id="cb543-112">Specifies an array of **DWORD** variables.</span></span> <span data-ttu-id="cb543-113">此記憶體會保留給路由通訊協定專用的資料。</span><span class="sxs-lookup"><span data-stu-id="cb543-113">This memory is reserved for data that is specific to routing protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb543-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb543-114">Requirements</span></span>



| <span data-ttu-id="cb543-115">需求</span><span class="sxs-lookup"><span data-stu-id="cb543-115">Requirement</span></span> | <span data-ttu-id="cb543-116">值</span><span class="sxs-lookup"><span data-stu-id="cb543-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cb543-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb543-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb543-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="cb543-118">None supported</span></span><br/>                                                        |
| <span data-ttu-id="cb543-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb543-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb543-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb543-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb543-121">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cb543-121">End of server support</span></span><br/>    | <span data-ttu-id="cb543-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb543-122">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="cb543-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cb543-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb543-124"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb543-124"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb543-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb543-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb543-126">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="cb543-126">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="cb543-127">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="cb543-127">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="cb543-128">**RTM \_ IP \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="cb543-128">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="cb543-129">**RTM \_ IPX \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="cb543-129">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





