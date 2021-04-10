---
title: Win32_RDSHCollection 類別的 KeyValueDelete 方法
description: 從集合中刪除指定的索引鍵 (以及相關聯的值) 。
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- KeyValueDelete 方法遠端桌面服務
- KeyValueDelete 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，KeyValueDelete 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934235"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="029b4-106">Win32 RDSHCollection 類別的 KeyValueDelete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="029b4-106">KeyValueDelete method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="029b4-107">從集合中刪除指定的索引鍵 (以及相關聯的值) 。</span><span class="sxs-lookup"><span data-stu-id="029b4-107">Deletes the specified key (and associated value) from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="029b4-108">語法</span><span class="sxs-lookup"><span data-stu-id="029b4-108">Syntax</span></span>


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="029b4-109">參數</span><span class="sxs-lookup"><span data-stu-id="029b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029b4-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="029b4-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="029b4-111">要刪除的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="029b4-111">The key to delete.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="029b4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="029b4-112">Requirements</span></span>



| <span data-ttu-id="029b4-113">需求</span><span class="sxs-lookup"><span data-stu-id="029b4-113">Requirement</span></span> | <span data-ttu-id="029b4-114">值</span><span class="sxs-lookup"><span data-stu-id="029b4-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="029b4-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="029b4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="029b4-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="029b4-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="029b4-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="029b4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="029b4-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="029b4-118">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="029b4-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="029b4-119">Namespace</span></span><br/>                | <span data-ttu-id="029b4-120">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="029b4-120">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="029b4-121">MOF</span><span class="sxs-lookup"><span data-stu-id="029b4-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="029b4-122"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="029b4-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="029b4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="029b4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="029b4-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="029b4-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="029b4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="029b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029b4-126">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="029b4-126">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





