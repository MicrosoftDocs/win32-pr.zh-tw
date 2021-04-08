---
description: 手寫筆離開 tablet 的實體偵測範圍 (近) 時發生。
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: ITabletEventSink：： CursorOutOfRange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852563"
---
# <a name="itableteventsinkcursoroutofrange-method"></a><span data-ttu-id="5b611-103">ITabletEventSink：： CursorOutOfRange 方法</span><span class="sxs-lookup"><span data-stu-id="5b611-103">ITabletEventSink::CursorOutOfRange method</span></span>

<span data-ttu-id="5b611-104">手寫筆離開 tablet 的實體偵測範圍 (近) 時發生。</span><span class="sxs-lookup"><span data-stu-id="5b611-104">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b611-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b611-105">Syntax</span></span>


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="5b611-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b611-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b611-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b611-108">Tablet 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b611-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="5b611-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="5b611-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="5b611-110">手寫筆的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b611-110">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b611-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b611-111">Return value</span></span>

<span data-ttu-id="5b611-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5b611-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5b611-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5b611-113">Return code</span></span>                                                                            | <span data-ttu-id="5b611-114">Description</span><span class="sxs-lookup"><span data-stu-id="5b611-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5b611-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5b611-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="5b611-116">成功。</span><span class="sxs-lookup"><span data-stu-id="5b611-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="5b611-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="5b611-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="5b611-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b611-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5b611-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b611-119">Requirements</span></span>



| <span data-ttu-id="5b611-120">需求</span><span class="sxs-lookup"><span data-stu-id="5b611-120">Requirement</span></span> | <span data-ttu-id="5b611-121">值</span><span class="sxs-lookup"><span data-stu-id="5b611-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b611-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b611-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b611-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b611-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5b611-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b611-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b611-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="5b611-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5b611-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b611-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b611-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b611-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b611-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b611-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b611-129">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="5b611-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




