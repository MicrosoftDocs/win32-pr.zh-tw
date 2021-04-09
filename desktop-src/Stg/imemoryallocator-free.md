---
title: IMemoryAllocator Free 方法
description: Free 方法會釋出配置方法所配置的記憶體。
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- 自由方法結構化儲存體
- 自由方法結構化儲存體、IMemoryAllocator 介面
- IMemoryAllocator 介面結構化儲存體，免費方法
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024694"
---
# <a name="imemoryallocatorfree-method"></a><span data-ttu-id="3c162-106">IMemoryAllocator：： Free 方法</span><span class="sxs-lookup"><span data-stu-id="3c162-106">IMemoryAllocator::Free method</span></span>

<span data-ttu-id="3c162-107">**Free** 方法會釋出配置方法所 [**配置**](imemoryallocator-allocate.md)的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3c162-107">The **Free** method frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c162-108">語法</span><span class="sxs-lookup"><span data-stu-id="3c162-108">Syntax</span></span>


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a><span data-ttu-id="3c162-109">參數</span><span class="sxs-lookup"><span data-stu-id="3c162-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c162-110">*光伏*</span><span class="sxs-lookup"><span data-stu-id="3c162-110">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="3c162-111">要釋放之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="3c162-111">Pointer to the memory to be freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c162-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c162-112">Requirements</span></span>



| <span data-ttu-id="3c162-113">需求</span><span class="sxs-lookup"><span data-stu-id="3c162-113">Requirement</span></span> | <span data-ttu-id="3c162-114">值</span><span class="sxs-lookup"><span data-stu-id="3c162-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3c162-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c162-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3c162-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c162-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3c162-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c162-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3c162-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c162-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3c162-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c162-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c162-120"><dt>Ole32.lib .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c162-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

 





