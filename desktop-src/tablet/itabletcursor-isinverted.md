---
description: 指出手寫筆是否已反轉。
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: ITabletCursor：： IsInverted 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983775"
---
# <a name="itabletcursorisinverted-method"></a><span data-ttu-id="a76dd-103">ITabletCursor：： IsInverted 方法</span><span class="sxs-lookup"><span data-stu-id="a76dd-103">ITabletCursor::IsInverted method</span></span>

<span data-ttu-id="a76dd-104">指出手寫筆是否已反轉。</span><span class="sxs-lookup"><span data-stu-id="a76dd-104">Indicates if the stylus is upside down.</span></span>

## <a name="syntax"></a><span data-ttu-id="a76dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="a76dd-105">Syntax</span></span>


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a><span data-ttu-id="a76dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="a76dd-106">Parameters</span></span>

<span data-ttu-id="a76dd-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a76dd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a76dd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a76dd-108">Return value</span></span>

<span data-ttu-id="a76dd-109">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a76dd-109">This method can return one of these values.</span></span>



| <span data-ttu-id="a76dd-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a76dd-110">Return code</span></span>                                                                             | <span data-ttu-id="a76dd-111">Description</span><span class="sxs-lookup"><span data-stu-id="a76dd-111">Description</span></span>                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a76dd-112"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a76dd-112"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a76dd-113">手寫筆已反轉。</span><span class="sxs-lookup"><span data-stu-id="a76dd-113">The stylus is inverted.</span></span><br/>        |
| <dl> <span data-ttu-id="a76dd-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a76dd-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a76dd-115">手寫筆未反轉。</span><span class="sxs-lookup"><span data-stu-id="a76dd-115">The stylus is not inverted.</span></span><br/>    |
| <dl> <span data-ttu-id="a76dd-116"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="a76dd-116"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="a76dd-117">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a76dd-117">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a76dd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a76dd-118">Requirements</span></span>



| <span data-ttu-id="a76dd-119">需求</span><span class="sxs-lookup"><span data-stu-id="a76dd-119">Requirement</span></span> | <span data-ttu-id="a76dd-120">值</span><span class="sxs-lookup"><span data-stu-id="a76dd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a76dd-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a76dd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a76dd-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a76dd-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a76dd-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a76dd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a76dd-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="a76dd-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a76dd-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a76dd-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a76dd-126"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a76dd-126"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a76dd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a76dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76dd-128">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="a76dd-128">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="a76dd-129">**ITabletCursorButton 介面**</span><span class="sxs-lookup"><span data-stu-id="a76dd-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




