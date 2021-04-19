---
description: 抓取 tablet 手寫筆上的按鈕數目。
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: ITabletCursor：： GetButtonCount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983878"
---
# <a name="itabletcursorgetbuttoncount-method"></a><span data-ttu-id="1a440-103">ITabletCursor：： GetButtonCount 方法</span><span class="sxs-lookup"><span data-stu-id="1a440-103">ITabletCursor::GetButtonCount method</span></span>

<span data-ttu-id="1a440-104">抓取 tablet 手寫筆上的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="1a440-104">Retrieves the number of buttons on the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a440-105">語法</span><span class="sxs-lookup"><span data-stu-id="1a440-105">Syntax</span></span>


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a><span data-ttu-id="1a440-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a440-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a440-107">*pcButtons* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1a440-107">*pcButtons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a440-108">Tablet 手寫筆上的按鈕計數。</span><span class="sxs-lookup"><span data-stu-id="1a440-108">The count of buttons on the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a440-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a440-109">Return value</span></span>

<span data-ttu-id="1a440-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1a440-110">This method can return one of these values.</span></span>



| <span data-ttu-id="1a440-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1a440-111">Return code</span></span>                                                                            | <span data-ttu-id="1a440-112">Description</span><span class="sxs-lookup"><span data-stu-id="1a440-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1a440-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1a440-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="1a440-114">成功。</span><span class="sxs-lookup"><span data-stu-id="1a440-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="1a440-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="1a440-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="1a440-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a440-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a440-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a440-117">Requirements</span></span>



| <span data-ttu-id="1a440-118">需求</span><span class="sxs-lookup"><span data-stu-id="1a440-118">Requirement</span></span> | <span data-ttu-id="1a440-119">值</span><span class="sxs-lookup"><span data-stu-id="1a440-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a440-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a440-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a440-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a440-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1a440-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a440-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a440-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="1a440-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1a440-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a440-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a440-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a440-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a440-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a440-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a440-127">**ITabletCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="1a440-127">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




