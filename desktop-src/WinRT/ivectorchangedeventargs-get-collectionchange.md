---
description: 取得在向量中發生的變更類型。
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'IVectorChangedEventArgs：： get_CollectionChange 方法 (IVectorChangedEventArgs .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191348"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a><span data-ttu-id="9362e-103">IVectorChangedEventArgs：： get \_ CollectionChange 方法</span><span class="sxs-lookup"><span data-stu-id="9362e-103">IVectorChangedEventArgs::get\_CollectionChange method</span></span>

<span data-ttu-id="9362e-104">取得在向量中發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="9362e-104">Gets the type of change that occurred in the vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9362e-105">語法</span><span class="sxs-lookup"><span data-stu-id="9362e-105">Syntax</span></span>


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a><span data-ttu-id="9362e-106">參數</span><span class="sxs-lookup"><span data-stu-id="9362e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9362e-107">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="9362e-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9362e-108">類型： \**CollectionChange \** _</span><span class="sxs-lookup"><span data-stu-id="9362e-108">Type: \**CollectionChange\** _</span></span>

<span data-ttu-id="9362e-109">描述變更之 [_ *CollectionChange* \*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041)列舉中的值。</span><span class="sxs-lookup"><span data-stu-id="9362e-109">A value from the [_ *CollectionChange*\*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) enumeration that describes the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9362e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9362e-110">Return value</span></span>

<span data-ttu-id="9362e-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9362e-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9362e-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9362e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9362e-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9362e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9362e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9362e-114">Requirements</span></span>



| <span data-ttu-id="9362e-115">需求</span><span class="sxs-lookup"><span data-stu-id="9362e-115">Requirement</span></span> | <span data-ttu-id="9362e-116">值</span><span class="sxs-lookup"><span data-stu-id="9362e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9362e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9362e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9362e-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9362e-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="9362e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9362e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9362e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9362e-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="9362e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9362e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9362e-122"><dt>IVectorChangedEventArgs。h</dt></span><span class="sxs-lookup"><span data-stu-id="9362e-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9362e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9362e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9362e-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="9362e-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 
