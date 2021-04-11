---
description: 抓取代表平板電腦最大輸入區域的矩形。
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: ITablet：： GetMaxInputRect 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850983"
---
# <a name="itabletgetmaxinputrect-method"></a><span data-ttu-id="4cb3f-103">ITablet：： GetMaxInputRect 方法</span><span class="sxs-lookup"><span data-stu-id="4cb3f-103">ITablet::GetMaxInputRect method</span></span>

<span data-ttu-id="4cb3f-104">抓取代表平板電腦最大輸入區域的矩形。</span><span class="sxs-lookup"><span data-stu-id="4cb3f-104">Retrieves a rectangle that represents maximum input area of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb3f-105">語法</span><span class="sxs-lookup"><span data-stu-id="4cb3f-105">Syntax</span></span>


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="4cb3f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4cb3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb3f-107">*prcInput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4cb3f-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb3f-108">代表平板電腦輸入區域最大值的矩形指標。</span><span class="sxs-lookup"><span data-stu-id="4cb3f-108">Pointer to rectangle that represents maximum input area of the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb3f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cb3f-109">Return value</span></span>

<span data-ttu-id="4cb3f-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4cb3f-110">This method can return one of these values.</span></span>



| <span data-ttu-id="4cb3f-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4cb3f-111">Return code</span></span>                                                                            | <span data-ttu-id="4cb3f-112">Description</span><span class="sxs-lookup"><span data-stu-id="4cb3f-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4cb3f-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb3f-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4cb3f-114">成功。</span><span class="sxs-lookup"><span data-stu-id="4cb3f-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="4cb3f-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb3f-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4cb3f-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4cb3f-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4cb3f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cb3f-117">Requirements</span></span>



| <span data-ttu-id="4cb3f-118">需求</span><span class="sxs-lookup"><span data-stu-id="4cb3f-118">Requirement</span></span> | <span data-ttu-id="4cb3f-119">值</span><span class="sxs-lookup"><span data-stu-id="4cb3f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb3f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cb3f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb3f-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cb3f-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4cb3f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cb3f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb3f-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="4cb3f-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4cb3f-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="4cb3f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="4cb3f-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4cb3f-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb3f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cb3f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb3f-127">**ITablet 介面**</span><span class="sxs-lookup"><span data-stu-id="4cb3f-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




