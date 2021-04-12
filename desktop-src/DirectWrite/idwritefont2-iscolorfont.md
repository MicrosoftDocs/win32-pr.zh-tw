---
title: IDWriteFont2 IsColorFont 方法
description: 可判斷是否有可能需要色彩轉譯路徑。
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- IsColorFont 方法直接寫入
- IsColorFont 方法 Direct Write，IDWriteFont2 介面
- IDWriteFont2 介面 Direct Write，IsColorFont 方法
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384922"
---
# <a name="idwritefont2iscolorfont-method"></a><span data-ttu-id="aede4-106">IDWriteFont2：： IsColorFont 方法</span><span class="sxs-lookup"><span data-stu-id="aede4-106">IDWriteFont2::IsColorFont method</span></span>

<span data-ttu-id="aede4-107">可判斷是否有可能需要色彩轉譯路徑。</span><span class="sxs-lookup"><span data-stu-id="aede4-107">Enables determining if a color rendering path is potentially necessary.</span></span>

## <a name="syntax"></a><span data-ttu-id="aede4-108">語法</span><span class="sxs-lookup"><span data-stu-id="aede4-108">Syntax</span></span>


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a><span data-ttu-id="aede4-109">參數</span><span class="sxs-lookup"><span data-stu-id="aede4-109">Parameters</span></span>

<span data-ttu-id="aede4-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="aede4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aede4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aede4-111">Return value</span></span>

<span data-ttu-id="aede4-112">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="aede4-112">Type: **BOOL**</span></span>

<span data-ttu-id="aede4-113">如果字型有 (COLR 和 CPAL 資料表的色彩資訊，則傳回 **TRUE** ，) ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="aede4-113">Returns **TRUE** if the font has color information (COLR and CPAL tables); otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aede4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="aede4-114">Requirements</span></span>



| <span data-ttu-id="aede4-115">需求</span><span class="sxs-lookup"><span data-stu-id="aede4-115">Requirement</span></span> | <span data-ttu-id="aede4-116">值</span><span class="sxs-lookup"><span data-stu-id="aede4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aede4-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aede4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aede4-118">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aede4-118">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="aede4-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aede4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aede4-120">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aede4-120">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="aede4-121">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="aede4-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="aede4-122">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aede4-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="aede4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="aede4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="aede4-124"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aede4-124"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="aede4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aede4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aede4-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aede4-126"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aede4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aede4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aede4-128">**IDWriteFont2**</span><span class="sxs-lookup"><span data-stu-id="aede4-128">**IDWriteFont2**</span></span>](idwritefont2.md)
</dt> </dl>

 

 





