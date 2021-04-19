---
description: 從 tablet 手寫筆取出指定的按鈕物件。
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: ITabletCursor：： GetButton 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985236"
---
# <a name="itabletcursorgetbutton-method"></a><span data-ttu-id="2fa3a-103">ITabletCursor：： GetButton 方法</span><span class="sxs-lookup"><span data-stu-id="2fa3a-103">ITabletCursor::GetButton method</span></span>

<span data-ttu-id="2fa3a-104">從 tablet 手寫筆取出指定的按鈕物件。</span><span class="sxs-lookup"><span data-stu-id="2fa3a-104">Retrieves the specified button object from a tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="2fa3a-105">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a><span data-ttu-id="2fa3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="2fa3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa3a-107">*iButton* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2fa3a-107">*iButton* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa3a-108">要取出之按鈕的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fa3a-108">Identifier of the button to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2fa3a-109">*ppButton* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2fa3a-109">*ppButton* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa3a-110">*IButton* 參數所指定的按鈕物件。</span><span class="sxs-lookup"><span data-stu-id="2fa3a-110">The button object specified by the *iButton* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa3a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fa3a-111">Return value</span></span>

<span data-ttu-id="2fa3a-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2fa3a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2fa3a-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2fa3a-113">Return code</span></span>                                                                            | <span data-ttu-id="2fa3a-114">Description</span><span class="sxs-lookup"><span data-stu-id="2fa3a-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2fa3a-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2fa3a-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="2fa3a-116">成功。</span><span class="sxs-lookup"><span data-stu-id="2fa3a-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="2fa3a-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="2fa3a-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="2fa3a-118">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2fa3a-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2fa3a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fa3a-119">Requirements</span></span>



| <span data-ttu-id="2fa3a-120">需求</span><span class="sxs-lookup"><span data-stu-id="2fa3a-120">Requirement</span></span> | <span data-ttu-id="2fa3a-121">值</span><span class="sxs-lookup"><span data-stu-id="2fa3a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa3a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fa3a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa3a-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fa3a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2fa3a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fa3a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa3a-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="2fa3a-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2fa3a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2fa3a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fa3a-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fa3a-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa3a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fa3a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa3a-129">**ITabletCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="2fa3a-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




