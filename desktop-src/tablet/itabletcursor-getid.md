---
description: 抓取手寫筆識別碼。
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: ITabletCursor：： GetId 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386254"
---
# <a name="itabletcursorgetid-method"></a><span data-ttu-id="e53df-103">ITabletCursor：： GetId 方法</span><span class="sxs-lookup"><span data-stu-id="e53df-103">ITabletCursor::GetId method</span></span>

<span data-ttu-id="e53df-104">抓取手寫筆識別碼。</span><span class="sxs-lookup"><span data-stu-id="e53df-104">Retrieves the stylus identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53df-105">語法</span><span class="sxs-lookup"><span data-stu-id="e53df-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a><span data-ttu-id="e53df-106">參數</span><span class="sxs-lookup"><span data-stu-id="e53df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e53df-107">*pCid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e53df-107">*pCid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e53df-108">Tablet 手寫筆的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e53df-108">The identifier of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e53df-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e53df-109">Return value</span></span>

<span data-ttu-id="e53df-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e53df-110">This method can return one of these values.</span></span>



| <span data-ttu-id="e53df-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e53df-111">Return code</span></span>                                                                            | <span data-ttu-id="e53df-112">Description</span><span class="sxs-lookup"><span data-stu-id="e53df-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e53df-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e53df-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e53df-114">成功。</span><span class="sxs-lookup"><span data-stu-id="e53df-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e53df-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e53df-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e53df-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e53df-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e53df-117">備註</span><span class="sxs-lookup"><span data-stu-id="e53df-117">Remarks</span></span>

<span data-ttu-id="e53df-118">資料指標 \_ 識別碼定義為 DWORD。</span><span class="sxs-lookup"><span data-stu-id="e53df-118">CURSOR\_ID is defined as a DWORD.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53df-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e53df-119">Requirements</span></span>



| <span data-ttu-id="e53df-120">需求</span><span class="sxs-lookup"><span data-stu-id="e53df-120">Requirement</span></span> | <span data-ttu-id="e53df-121">值</span><span class="sxs-lookup"><span data-stu-id="e53df-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e53df-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e53df-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e53df-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e53df-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e53df-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e53df-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e53df-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="e53df-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e53df-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e53df-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e53df-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e53df-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e53df-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e53df-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53df-129">**ITabletCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="e53df-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




