---
description: 將 tablet 內容移至輸入佇列的前端或背面。
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: ITabletCoNtextP：：重迭方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990404"
---
# <a name="itabletcontextpoverlap-method"></a><span data-ttu-id="d171c-103">ITabletCoNtextP：：重迭方法</span><span class="sxs-lookup"><span data-stu-id="d171c-103">ITabletContextP::Overlap method</span></span>

<span data-ttu-id="d171c-104">將 tablet 內容移至輸入佇列的前端或背面。</span><span class="sxs-lookup"><span data-stu-id="d171c-104">Moves a tablet context to the front or back of the input queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="d171c-105">語法</span><span class="sxs-lookup"><span data-stu-id="d171c-105">Syntax</span></span>


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a><span data-ttu-id="d171c-106">參數</span><span class="sxs-lookup"><span data-stu-id="d171c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d171c-107">*bTop* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d171c-107">*bTop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d171c-108">表示 tablet 內容是否應該移至輸入佇列的頂端或底部。</span><span class="sxs-lookup"><span data-stu-id="d171c-108">Indicates if the tablet context should be moved to the top or bottom of the input queue.</span></span>

</dd> <dt>

<span data-ttu-id="d171c-109">*pdwtcid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d171c-109">*pdwtcid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d171c-110">Tablet 內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="d171c-110">The tablet context identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d171c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d171c-111">Return value</span></span>

<span data-ttu-id="d171c-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d171c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d171c-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d171c-113">Return code</span></span>                                                                            | <span data-ttu-id="d171c-114">Description</span><span class="sxs-lookup"><span data-stu-id="d171c-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d171c-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d171c-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d171c-116">成功。</span><span class="sxs-lookup"><span data-stu-id="d171c-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d171c-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d171c-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d171c-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d171c-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d171c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d171c-119">Requirements</span></span>



| <span data-ttu-id="d171c-120">需求</span><span class="sxs-lookup"><span data-stu-id="d171c-120">Requirement</span></span> | <span data-ttu-id="d171c-121">值</span><span class="sxs-lookup"><span data-stu-id="d171c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d171c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d171c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d171c-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d171c-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d171c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d171c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d171c-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="d171c-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d171c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d171c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d171c-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d171c-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d171c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d171c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d171c-129">**ITabletCoNtextP 介面**</span><span class="sxs-lookup"><span data-stu-id="d171c-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




