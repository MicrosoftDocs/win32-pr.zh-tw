---
description: 發生于游標移至 tablet 數位化板上時。
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: ITabletEventSink：： CursorMove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000325"
---
# <a name="itableteventsinkcursormove-method"></a><span data-ttu-id="b7114-103">ITabletEventSink：： CursorMove 方法</span><span class="sxs-lookup"><span data-stu-id="b7114-103">ITabletEventSink::CursorMove method</span></span>

<span data-ttu-id="b7114-104">發生于游標移至 tablet 數位化板上時。</span><span class="sxs-lookup"><span data-stu-id="b7114-104">Occurs when the cursor moves over the tablet digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7114-105">語法</span><span class="sxs-lookup"><span data-stu-id="b7114-105">Syntax</span></span>


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a><span data-ttu-id="b7114-106">參數</span><span class="sxs-lookup"><span data-stu-id="b7114-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7114-107">*tcid*</span><span class="sxs-lookup"><span data-stu-id="b7114-107">*tcid*</span></span> 
</dt> <dd>

<span data-ttu-id="b7114-108">Tablet 數位板的唯一 dentifier。</span><span class="sxs-lookup"><span data-stu-id="b7114-108">Unique dentifier of the tablet digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="b7114-109">*Cid*</span><span class="sxs-lookup"><span data-stu-id="b7114-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="b7114-110">Tablet 手寫筆的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7114-110">Unique identifier of the tablet stylus.</span></span>

</dd> <dt>

<span data-ttu-id="b7114-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="b7114-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b7114-112">移動資料指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="b7114-112">The window over which the cursor moved.</span></span>

</dd> <dt>

<span data-ttu-id="b7114-113">*xPos*</span><span class="sxs-lookup"><span data-stu-id="b7114-113">*xPos*</span></span> 
</dt> <dd>

<span data-ttu-id="b7114-114">手寫筆的 X 位置。</span><span class="sxs-lookup"><span data-stu-id="b7114-114">The X position of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="b7114-115">*yPos*</span><span class="sxs-lookup"><span data-stu-id="b7114-115">*yPos*</span></span> 
</dt> <dd>

<span data-ttu-id="b7114-116">手寫筆的 Y 位置。</span><span class="sxs-lookup"><span data-stu-id="b7114-116">The Y position of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7114-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7114-117">Return value</span></span>

<span data-ttu-id="b7114-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b7114-118">This method can return one of these values.</span></span>



| <span data-ttu-id="b7114-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b7114-119">Return code</span></span>                                                                            | <span data-ttu-id="b7114-120">Description</span><span class="sxs-lookup"><span data-stu-id="b7114-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="b7114-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b7114-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b7114-122">成功。</span><span class="sxs-lookup"><span data-stu-id="b7114-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="b7114-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="b7114-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b7114-124">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7114-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b7114-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7114-125">Requirements</span></span>



| <span data-ttu-id="b7114-126">需求</span><span class="sxs-lookup"><span data-stu-id="b7114-126">Requirement</span></span> | <span data-ttu-id="b7114-127">值</span><span class="sxs-lookup"><span data-stu-id="b7114-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7114-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7114-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b7114-129">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7114-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b7114-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7114-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b7114-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="b7114-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b7114-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7114-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7114-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7114-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7114-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7114-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7114-135">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="b7114-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




