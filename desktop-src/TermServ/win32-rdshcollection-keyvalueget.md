---
title: Win32_RDSHCollection 類別的 KeyValueGet 方法
description: 抓取與集合中指定之索引鍵相關聯的值。
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- KeyValueGet 方法遠端桌面服務
- KeyValueGet 方法遠端桌面服務，Win32_RDSHCollection 類別
- Win32_RDSHCollection 類別遠端桌面服務，KeyValueGet 方法
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843392"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="ffbf6-106">Win32 RDSHCollection 類別的 KeyValueGet 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ffbf6-106">KeyValueGet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="ffbf6-107">抓取與集合中指定之索引鍵相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="ffbf6-107">Retrieves the value associated with the specified key in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbf6-108">語法</span><span class="sxs-lookup"><span data-stu-id="ffbf6-108">Syntax</span></span>


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="ffbf6-109">參數</span><span class="sxs-lookup"><span data-stu-id="ffbf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffbf6-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffbf6-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffbf6-111">識別您想要取得之值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ffbf6-111">The key that identifies the value you wish to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ffbf6-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ffbf6-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffbf6-113">成功時，傳回與指定索引鍵相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="ffbf6-113">On success, returns the value associated with the specified key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffbf6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffbf6-114">Requirements</span></span>



| <span data-ttu-id="ffbf6-115">需求</span><span class="sxs-lookup"><span data-stu-id="ffbf6-115">Requirement</span></span> | <span data-ttu-id="ffbf6-116">值</span><span class="sxs-lookup"><span data-stu-id="ffbf6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbf6-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffbf6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ffbf6-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="ffbf6-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ffbf6-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffbf6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ffbf6-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ffbf6-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="ffbf6-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="ffbf6-121">Namespace</span></span><br/>                | <span data-ttu-id="ffbf6-122">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="ffbf6-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ffbf6-123">MOF</span><span class="sxs-lookup"><span data-stu-id="ffbf6-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffbf6-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffbf6-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffbf6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ffbf6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffbf6-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffbf6-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ffbf6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffbf6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbf6-128">**Win32 \_ RDSHCollection**</span><span class="sxs-lookup"><span data-stu-id="ffbf6-128">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





