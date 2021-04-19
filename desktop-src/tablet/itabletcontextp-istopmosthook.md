---
description: 指出 tablet 內容是否在最上層的掛勾中。
ms.assetid: b4aaee47-3d77-49cd-9600-f41764b9fb85
title: ITabletCoNtextP：： IsTopMostHook 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.IsTopMostHook
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: f62de678085bda723bb13a721d75c349d395787a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997945"
---
# <a name="itabletcontextpistopmosthook-method"></a><span data-ttu-id="1524c-103">ITabletCoNtextP：： IsTopMostHook 方法</span><span class="sxs-lookup"><span data-stu-id="1524c-103">ITabletContextP::IsTopMostHook method</span></span>

<span data-ttu-id="1524c-104">指出 tablet 內容是否在最上層的掛勾中。</span><span class="sxs-lookup"><span data-stu-id="1524c-104">Indicates if the tablet context is in the top most hook.</span></span>

## <a name="syntax"></a><span data-ttu-id="1524c-105">語法</span><span class="sxs-lookup"><span data-stu-id="1524c-105">Syntax</span></span>


```C++
HRESULT IsTopMostHook();
```



## <a name="parameters"></a><span data-ttu-id="1524c-106">參數</span><span class="sxs-lookup"><span data-stu-id="1524c-106">Parameters</span></span>

<span data-ttu-id="1524c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1524c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1524c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1524c-108">Return value</span></span>

<span data-ttu-id="1524c-109">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1524c-109">This method can return one of these values.</span></span>



| <span data-ttu-id="1524c-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1524c-110">Return code</span></span>                                                                            | <span data-ttu-id="1524c-111">Description</span><span class="sxs-lookup"><span data-stu-id="1524c-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1524c-112"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1524c-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="1524c-113">成功。</span><span class="sxs-lookup"><span data-stu-id="1524c-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="1524c-114"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="1524c-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="1524c-115">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1524c-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1524c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1524c-116">Requirements</span></span>



| <span data-ttu-id="1524c-117">需求</span><span class="sxs-lookup"><span data-stu-id="1524c-117">Requirement</span></span> | <span data-ttu-id="1524c-118">值</span><span class="sxs-lookup"><span data-stu-id="1524c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1524c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1524c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1524c-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1524c-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1524c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1524c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1524c-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="1524c-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1524c-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="1524c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1524c-124"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1524c-124"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1524c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1524c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1524c-126">**ITabletCoNtextP 介面**</span><span class="sxs-lookup"><span data-stu-id="1524c-126">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




