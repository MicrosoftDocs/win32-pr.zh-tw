---
description: 捕獲 tablet 手寫筆的名稱。
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: ITabletCursor：： GetName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945162"
---
# <a name="itabletcursorgetname-method"></a><span data-ttu-id="28421-103">ITabletCursor：： GetName 方法</span><span class="sxs-lookup"><span data-stu-id="28421-103">ITabletCursor::GetName method</span></span>

<span data-ttu-id="28421-104">捕獲 tablet 手寫筆的名稱。</span><span class="sxs-lookup"><span data-stu-id="28421-104">Retrieves the name of the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="28421-105">語法</span><span class="sxs-lookup"><span data-stu-id="28421-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="28421-106">參數</span><span class="sxs-lookup"><span data-stu-id="28421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28421-107">*ppwszName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28421-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28421-108">Tablet 手寫筆的名稱。</span><span class="sxs-lookup"><span data-stu-id="28421-108">The name of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28421-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="28421-109">Return value</span></span>

<span data-ttu-id="28421-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="28421-110">This method can return one of these values.</span></span>



| <span data-ttu-id="28421-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="28421-111">Return code</span></span>                                                                            | <span data-ttu-id="28421-112">Description</span><span class="sxs-lookup"><span data-stu-id="28421-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="28421-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="28421-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="28421-114">成功。</span><span class="sxs-lookup"><span data-stu-id="28421-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="28421-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="28421-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="28421-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="28421-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28421-117">備註</span><span class="sxs-lookup"><span data-stu-id="28421-117">Remarks</span></span>

<span data-ttu-id="28421-118">呼叫端會負責使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)釋放從此方法傳回的記憶體。</span><span class="sxs-lookup"><span data-stu-id="28421-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="28421-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="28421-119">Requirements</span></span>



| <span data-ttu-id="28421-120">需求</span><span class="sxs-lookup"><span data-stu-id="28421-120">Requirement</span></span> | <span data-ttu-id="28421-121">值</span><span class="sxs-lookup"><span data-stu-id="28421-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28421-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28421-122">Minimum supported client</span></span><br/> | <span data-ttu-id="28421-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28421-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="28421-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28421-124">Minimum supported server</span></span><br/> | <span data-ttu-id="28421-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="28421-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="28421-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="28421-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="28421-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28421-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28421-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28421-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28421-129">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="28421-129">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="28421-130">**ITabletCursorButton 介面**</span><span class="sxs-lookup"><span data-stu-id="28421-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

