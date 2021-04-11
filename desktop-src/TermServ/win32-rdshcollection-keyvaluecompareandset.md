---
title: Win32_RDSHCollection 類別的 KeyValueCompareAndSet 方法
description: 比較集合中指定的索引鍵與比較元;如果相符，索引鍵會設定為新的值。 如果索引鍵不存在，方法會將索引鍵插入集合中。
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- KeyValueCompareAndSet 方法遠端桌面服務
- KeyValueCompareAndSet 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，KeyValueCompareAndSet 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843395"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="3253c-107">Win32 RDSHCollection 類別的 KeyValueCompareAndSet 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3253c-107">KeyValueCompareAndSet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="3253c-108">比較集合中指定的索引鍵與比較元;如果相符，索引鍵會設定為新的值。</span><span class="sxs-lookup"><span data-stu-id="3253c-108">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="3253c-109">如果索引鍵不存在，方法會將索引鍵插入集合中。</span><span class="sxs-lookup"><span data-stu-id="3253c-109">If the key does not exist, the method will insert the key into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3253c-110">語法</span><span class="sxs-lookup"><span data-stu-id="3253c-110">Syntax</span></span>


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a><span data-ttu-id="3253c-111">參數</span><span class="sxs-lookup"><span data-stu-id="3253c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3253c-112">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3253c-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3253c-113">要比較的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3253c-113">The key to compare.</span></span>

</dd> <dt>

<span data-ttu-id="3253c-114">*NewValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3253c-114">*NewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3253c-115">新值。</span><span class="sxs-lookup"><span data-stu-id="3253c-115">The new value.</span></span>

</dd> <dt>

<span data-ttu-id="3253c-116">*比較元* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3253c-116">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3253c-117">要用來比較索引鍵的字串。</span><span class="sxs-lookup"><span data-stu-id="3253c-117">The string to compare the key to.</span></span>

</dd> <dt>

<span data-ttu-id="3253c-118">*InitialValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3253c-118">*InitialValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3253c-119">在成功或失敗時，會包含索引鍵的起始值。</span><span class="sxs-lookup"><span data-stu-id="3253c-119">On success or failure, contains the initial value of the key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3253c-120">備註</span><span class="sxs-lookup"><span data-stu-id="3253c-120">Remarks</span></span>

<span data-ttu-id="3253c-121">請注意，這個方法可以取出索引鍵的值，因此會封裝 [**KeyValueGet**](win32-rdshcollection-keyvalueget.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="3253c-121">Note that this method can retrieve the value of the key, and as such encapsulates the functionality of [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3253c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3253c-122">Requirements</span></span>



| <span data-ttu-id="3253c-123">需求</span><span class="sxs-lookup"><span data-stu-id="3253c-123">Requirement</span></span> | <span data-ttu-id="3253c-124">值</span><span class="sxs-lookup"><span data-stu-id="3253c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3253c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3253c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3253c-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="3253c-126">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3253c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3253c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3253c-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3253c-128">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="3253c-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="3253c-129">Namespace</span></span><br/>                | <span data-ttu-id="3253c-130">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="3253c-130">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3253c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3253c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3253c-132"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="3253c-132"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3253c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3253c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3253c-134"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3253c-134"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3253c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3253c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3253c-136">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="3253c-136">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





