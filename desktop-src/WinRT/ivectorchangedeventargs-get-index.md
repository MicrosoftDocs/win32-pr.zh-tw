---
description: 取得向量中發生變更的位置。
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'IVectorChangedEventArgs：： get_Index 方法 (IVectorChangedEventArgs .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026224"
---
# <a name="ivectorchangedeventargsget_index-method"></a><span data-ttu-id="4709f-103">IVectorChangedEventArgs：： get \_ Index 方法</span><span class="sxs-lookup"><span data-stu-id="4709f-103">IVectorChangedEventArgs::get\_Index method</span></span>

<span data-ttu-id="4709f-104">取得向量中發生變更的位置。</span><span class="sxs-lookup"><span data-stu-id="4709f-104">Gets the position in the vector where the change occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="4709f-105">語法</span><span class="sxs-lookup"><span data-stu-id="4709f-105">Syntax</span></span>


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a><span data-ttu-id="4709f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4709f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4709f-107">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4709f-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4709f-108">類型： \**未 \* 簽署* _</span><span class="sxs-lookup"><span data-stu-id="4709f-108">Type: \**unsigned\** _</span></span>

<span data-ttu-id="4709f-109">向量中發生變更之以零為起始的位置（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="4709f-109">The zero-based position in the vector where the change occurred, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4709f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4709f-110">Return value</span></span>

<span data-ttu-id="4709f-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4709f-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4709f-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4709f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4709f-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4709f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4709f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4709f-114">Requirements</span></span>



| <span data-ttu-id="4709f-115">需求</span><span class="sxs-lookup"><span data-stu-id="4709f-115">Requirement</span></span> | <span data-ttu-id="4709f-116">值</span><span class="sxs-lookup"><span data-stu-id="4709f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4709f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4709f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4709f-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4709f-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="4709f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4709f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4709f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4709f-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="4709f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4709f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4709f-122"><dt>IVectorChangedEventArgs。h</dt></span><span class="sxs-lookup"><span data-stu-id="4709f-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4709f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4709f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4709f-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="4709f-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 




