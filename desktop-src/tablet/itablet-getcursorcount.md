---
description: 傳回與平板電腦相關聯的資料指標物件數目。
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: ITablet：： GetCursorCount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975440"
---
# <a name="itabletgetcursorcount-method"></a><span data-ttu-id="2f7c4-103">ITablet：： GetCursorCount 方法</span><span class="sxs-lookup"><span data-stu-id="2f7c4-103">ITablet::GetCursorCount method</span></span>

<span data-ttu-id="2f7c4-104">傳回與平板電腦相關聯的資料指標物件數目。</span><span class="sxs-lookup"><span data-stu-id="2f7c4-104">Returns the number of cursor objects associated with the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f7c4-105">Syntax</span></span>


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a><span data-ttu-id="2f7c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f7c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7c4-107">*pcCurs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f7c4-107">*pcCurs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7c4-108">與平板電腦相關聯的資料指標物件數目。</span><span class="sxs-lookup"><span data-stu-id="2f7c4-108">The number of cursor objects associated with the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7c4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f7c4-109">Return value</span></span>

<span data-ttu-id="2f7c4-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2f7c4-110">This method can return one of these values.</span></span>



| <span data-ttu-id="2f7c4-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2f7c4-111">Return code</span></span>                                                                            | <span data-ttu-id="2f7c4-112">Description</span><span class="sxs-lookup"><span data-stu-id="2f7c4-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2f7c4-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2f7c4-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="2f7c4-114">成功。</span><span class="sxs-lookup"><span data-stu-id="2f7c4-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="2f7c4-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="2f7c4-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="2f7c4-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f7c4-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2f7c4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f7c4-117">Requirements</span></span>



| <span data-ttu-id="2f7c4-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f7c4-118">Requirement</span></span> | <span data-ttu-id="2f7c4-119">值</span><span class="sxs-lookup"><span data-stu-id="2f7c4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7c4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f7c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7c4-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f7c4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2f7c4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f7c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7c4-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="2f7c4-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2f7c4-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f7c4-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f7c4-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f7c4-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7c4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f7c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7c4-127">**ITablet 介面**</span><span class="sxs-lookup"><span data-stu-id="2f7c4-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




