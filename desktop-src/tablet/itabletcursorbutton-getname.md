---
description: 抓取手寫筆按鈕的名稱。
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: ITabletCursorButton：： GetName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980326"
---
# <a name="itabletcursorbuttongetname-method"></a><span data-ttu-id="5cb82-103">ITabletCursorButton：： GetName 方法</span><span class="sxs-lookup"><span data-stu-id="5cb82-103">ITabletCursorButton::GetName method</span></span>

<span data-ttu-id="5cb82-104">抓取手寫筆按鈕的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cb82-104">Retrieves the name of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb82-105">語法</span><span class="sxs-lookup"><span data-stu-id="5cb82-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="5cb82-106">參數</span><span class="sxs-lookup"><span data-stu-id="5cb82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb82-107">*ppwszName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5cb82-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cb82-108">手寫筆按鈕的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cb82-108">The name of the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cb82-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5cb82-109">Return value</span></span>

<span data-ttu-id="5cb82-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5cb82-110">This method can return one of these values.</span></span>



| <span data-ttu-id="5cb82-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5cb82-111">Return code</span></span>                                                                            | <span data-ttu-id="5cb82-112">Description</span><span class="sxs-lookup"><span data-stu-id="5cb82-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="5cb82-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5cb82-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="5cb82-114">成功。</span><span class="sxs-lookup"><span data-stu-id="5cb82-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="5cb82-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="5cb82-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="5cb82-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5cb82-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5cb82-117">備註</span><span class="sxs-lookup"><span data-stu-id="5cb82-117">Remarks</span></span>

<span data-ttu-id="5cb82-118">呼叫端會負責使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)釋放從此方法傳回的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5cb82-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb82-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cb82-119">Requirements</span></span>



| <span data-ttu-id="5cb82-120">需求</span><span class="sxs-lookup"><span data-stu-id="5cb82-120">Requirement</span></span> | <span data-ttu-id="5cb82-121">值</span><span class="sxs-lookup"><span data-stu-id="5cb82-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb82-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5cb82-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5cb82-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cb82-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5cb82-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5cb82-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5cb82-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="5cb82-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5cb82-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5cb82-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5cb82-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5cb82-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb82-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cb82-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb82-129">**ITabletCursorButton 介面**</span><span class="sxs-lookup"><span data-stu-id="5cb82-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

