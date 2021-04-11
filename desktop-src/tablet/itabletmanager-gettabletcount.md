---
description: 抓取連接至系統的平板電腦數目。
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: ITabletManager：： GetTabletCount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195110"
---
# <a name="itabletmanagergettabletcount-method"></a><span data-ttu-id="ac707-103">ITabletManager：： GetTabletCount 方法</span><span class="sxs-lookup"><span data-stu-id="ac707-103">ITabletManager::GetTabletCount method</span></span>

<span data-ttu-id="ac707-104">抓取連接至系統的平板電腦數目。</span><span class="sxs-lookup"><span data-stu-id="ac707-104">Retrieves the number of tablets attached to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac707-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac707-105">Syntax</span></span>


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a><span data-ttu-id="ac707-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac707-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac707-107">*pcTablets* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ac707-107">*pcTablets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac707-108">連接至系統的平板電腦數目。</span><span class="sxs-lookup"><span data-stu-id="ac707-108">The number of tablets attached to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac707-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac707-109">Return value</span></span>

<span data-ttu-id="ac707-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ac707-110">This method can return one of these values.</span></span>



| <span data-ttu-id="ac707-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ac707-111">Return code</span></span>                                                                            | <span data-ttu-id="ac707-112">Description</span><span class="sxs-lookup"><span data-stu-id="ac707-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ac707-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ac707-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ac707-114">成功。</span><span class="sxs-lookup"><span data-stu-id="ac707-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ac707-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="ac707-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ac707-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ac707-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac707-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac707-117">Requirements</span></span>



| <span data-ttu-id="ac707-118">需求</span><span class="sxs-lookup"><span data-stu-id="ac707-118">Requirement</span></span> | <span data-ttu-id="ac707-119">值</span><span class="sxs-lookup"><span data-stu-id="ac707-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac707-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac707-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac707-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac707-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ac707-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac707-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac707-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="ac707-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ac707-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac707-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac707-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac707-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac707-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac707-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac707-127">**ITabletManager 介面**</span><span class="sxs-lookup"><span data-stu-id="ac707-127">**ITabletManager Interface**</span></span>](itabletmanager.md)
</dt> </dl>

 

 




