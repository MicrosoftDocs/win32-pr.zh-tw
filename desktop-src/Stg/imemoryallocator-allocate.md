---
title: IMemoryAllocator 配置方法
description: 當函數將 SERIALIZEDPROPERTYVALUE 資料類型轉換成 PROPVARIANT 資料類型時，配置方法會為 StgConvertPropertyToVariant 函數配置記憶體。
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- 配置方法結構化儲存體
- 配置方法結構化儲存體、IMemoryAllocator 介面
- IMemoryAllocator 介面結構化儲存體，配置方法
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967310"
---
# <a name="imemoryallocatorallocate-method"></a><span data-ttu-id="3137c-106">IMemoryAllocator：： Allocate 方法</span><span class="sxs-lookup"><span data-stu-id="3137c-106">IMemoryAllocator::Allocate method</span></span>

<span data-ttu-id="3137c-107">當函數將 **SERIALIZEDPROPERTYVALUE** 資料類型轉換成 **PROPVARIANT** 資料類型時，配置方法會為 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)函數 **配置** 記憶體。</span><span class="sxs-lookup"><span data-stu-id="3137c-107">The **Allocate** method allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3137c-108">語法</span><span class="sxs-lookup"><span data-stu-id="3137c-108">Syntax</span></span>


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="3137c-109">參數</span><span class="sxs-lookup"><span data-stu-id="3137c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3137c-110">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3137c-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3137c-111">指定要配置的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="3137c-111">Specifies the size of memory to be allocated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3137c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3137c-112">Requirements</span></span>



| <span data-ttu-id="3137c-113">需求</span><span class="sxs-lookup"><span data-stu-id="3137c-113">Requirement</span></span> | <span data-ttu-id="3137c-114">值</span><span class="sxs-lookup"><span data-stu-id="3137c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3137c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3137c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3137c-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3137c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3137c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3137c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3137c-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3137c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3137c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="3137c-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="3137c-120"><dt>Ole32.lib .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3137c-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

