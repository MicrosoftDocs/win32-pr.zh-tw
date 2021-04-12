---
description: 當新的手寫筆新增至系統時發生。
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: ITabletEventSink：： CursorNew 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195113"
---
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="c24e2-103">ITabletEventSink：： CursorNew 方法</span><span class="sxs-lookup"><span data-stu-id="c24e2-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="c24e2-104">當新的手寫筆新增至系統時發生。</span><span class="sxs-lookup"><span data-stu-id="c24e2-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c24e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c24e2-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="c24e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c24e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c24e2-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c24e2-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c24e2-108">新增手寫筆的 tablet coNtext 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c24e2-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="c24e2-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="c24e2-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="c24e2-110">新手寫筆物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c24e2-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c24e2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c24e2-111">Return value</span></span>

<span data-ttu-id="c24e2-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c24e2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c24e2-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c24e2-113">Return code</span></span>                                                                            | <span data-ttu-id="c24e2-114">Description</span><span class="sxs-lookup"><span data-stu-id="c24e2-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c24e2-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c24e2-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c24e2-116">成功。</span><span class="sxs-lookup"><span data-stu-id="c24e2-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="c24e2-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="c24e2-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c24e2-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c24e2-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c24e2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c24e2-119">Requirements</span></span>



| <span data-ttu-id="c24e2-120">需求</span><span class="sxs-lookup"><span data-stu-id="c24e2-120">Requirement</span></span> | <span data-ttu-id="c24e2-121">值</span><span class="sxs-lookup"><span data-stu-id="c24e2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c24e2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c24e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c24e2-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c24e2-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c24e2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c24e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c24e2-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="c24e2-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c24e2-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c24e2-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c24e2-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c24e2-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c24e2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c24e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c24e2-129">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="c24e2-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




