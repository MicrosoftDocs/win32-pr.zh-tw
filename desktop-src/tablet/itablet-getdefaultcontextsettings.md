---
description: 捕獲平板電腦的預設內容設定。
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: ITablet：： GetDefaultCoNtextSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7e2f0977257553d8405b337dcc1f22d8b0fdff5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693540"
---
# <a name="itabletgetdefaultcontextsettings-method"></a><span data-ttu-id="9921b-103">ITablet：： GetDefaultCoNtextSettings 方法</span><span class="sxs-lookup"><span data-stu-id="9921b-103">ITablet::GetDefaultContextSettings method</span></span>

<span data-ttu-id="9921b-104">捕獲平板電腦的預設內容設定。</span><span class="sxs-lookup"><span data-stu-id="9921b-104">Retrieves the default context settings for the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="9921b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9921b-105">Syntax</span></span>


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a><span data-ttu-id="9921b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9921b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9921b-107">*ppTCS* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9921b-107">*ppTCS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9921b-108">平板電腦的預設內容設定。</span><span class="sxs-lookup"><span data-stu-id="9921b-108">The default context settings for the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9921b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9921b-109">Return value</span></span>

<span data-ttu-id="9921b-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9921b-110">This method can return one of these values.</span></span>



| <span data-ttu-id="9921b-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9921b-111">Return code</span></span>                                                                            | <span data-ttu-id="9921b-112">Description</span><span class="sxs-lookup"><span data-stu-id="9921b-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9921b-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9921b-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="9921b-114">成功。</span><span class="sxs-lookup"><span data-stu-id="9921b-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="9921b-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="9921b-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="9921b-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9921b-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9921b-117">備註</span><span class="sxs-lookup"><span data-stu-id="9921b-117">Remarks</span></span>

<span data-ttu-id="9921b-118">呼叫端會負責使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)釋放從此方法傳回的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9921b-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="9921b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9921b-119">Requirements</span></span>



| <span data-ttu-id="9921b-120">需求</span><span class="sxs-lookup"><span data-stu-id="9921b-120">Requirement</span></span> | <span data-ttu-id="9921b-121">值</span><span class="sxs-lookup"><span data-stu-id="9921b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9921b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9921b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9921b-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9921b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9921b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9921b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9921b-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="9921b-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9921b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="9921b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9921b-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9921b-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9921b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9921b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9921b-129">**ITablet 介面**</span><span class="sxs-lookup"><span data-stu-id="9921b-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

