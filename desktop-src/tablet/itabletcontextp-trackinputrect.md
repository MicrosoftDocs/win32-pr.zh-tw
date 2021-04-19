---
description: 將 tablet 數位板更新為視窗位置對應座標。
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: ITabletCoNtextP：： TrackInputRect 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985343"
---
# <a name="itabletcontextptrackinputrect-method"></a><span data-ttu-id="8b9ca-103">ITabletCoNtextP：： TrackInputRect 方法</span><span class="sxs-lookup"><span data-stu-id="8b9ca-103">ITabletContextP::TrackInputRect method</span></span>

<span data-ttu-id="8b9ca-104">將 tablet 數位板更新為視窗位置對應座標。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-104">Updates the tablet digitizer to window location mapping coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="8b9ca-105">Syntax</span></span>


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="8b9ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="8b9ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b9ca-107">*prcInput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8b9ca-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b9ca-108">在更新視窗和數位板座標之間的對應之後，新的輸入視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-108">The new input window rectangle after updating the mapping between the window and digitizer coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b9ca-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b9ca-109">Return value</span></span>

<span data-ttu-id="8b9ca-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-110">This method can return one of these values.</span></span>



| <span data-ttu-id="8b9ca-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8b9ca-111">Return code</span></span>                                                                            | <span data-ttu-id="8b9ca-112">Description</span><span class="sxs-lookup"><span data-stu-id="8b9ca-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8b9ca-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8b9ca-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8b9ca-114">成功。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8b9ca-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="8b9ca-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8b9ca-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b9ca-117">備註</span><span class="sxs-lookup"><span data-stu-id="8b9ca-117">Remarks</span></span>

<span data-ttu-id="8b9ca-118">每當畫面上視窗的位置變更時，就呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-118">Call this method anytime the location of the window on the screen changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9ca-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b9ca-119">Requirements</span></span>



| <span data-ttu-id="8b9ca-120">需求</span><span class="sxs-lookup"><span data-stu-id="8b9ca-120">Requirement</span></span> | <span data-ttu-id="8b9ca-121">值</span><span class="sxs-lookup"><span data-stu-id="8b9ca-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9ca-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b9ca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9ca-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b9ca-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8b9ca-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b9ca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9ca-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="8b9ca-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8b9ca-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8b9ca-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b9ca-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b9ca-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b9ca-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b9ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9ca-129">**ITabletCoNtextP 介面**</span><span class="sxs-lookup"><span data-stu-id="8b9ca-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




