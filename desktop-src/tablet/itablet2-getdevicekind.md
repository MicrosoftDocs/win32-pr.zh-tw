---
description: 傳回 tablet 物件所代表的硬體裝置類型，例如滑鼠、畫筆或觸控。
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: ITablet2：： GetDeviceKind 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995846"
---
# <a name="itablet2getdevicekind-method"></a><span data-ttu-id="978b0-103">ITablet2：： GetDeviceKind 方法</span><span class="sxs-lookup"><span data-stu-id="978b0-103">ITablet2::GetDeviceKind method</span></span>

<span data-ttu-id="978b0-104">傳回 tablet 物件所代表的硬體裝置類型，例如滑鼠、畫筆或觸控。</span><span class="sxs-lookup"><span data-stu-id="978b0-104">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span>

## <a name="syntax"></a><span data-ttu-id="978b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="978b0-105">Syntax</span></span>


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a><span data-ttu-id="978b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="978b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978b0-107">*pKind* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="978b0-107">*pKind* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="978b0-108">列舉值，指出平板電腦的類型，例如滑鼠、畫筆或觸控。</span><span class="sxs-lookup"><span data-stu-id="978b0-108">Enumeration value that indicates the type of tablet such as mouse, pen or touch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978b0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="978b0-109">Return value</span></span>

<span data-ttu-id="978b0-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="978b0-110">This method can return one of these values.</span></span>



| <span data-ttu-id="978b0-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="978b0-111">Return code</span></span>                                                                            | <span data-ttu-id="978b0-112">Description</span><span class="sxs-lookup"><span data-stu-id="978b0-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="978b0-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="978b0-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="978b0-114">成功。</span><span class="sxs-lookup"><span data-stu-id="978b0-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="978b0-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="978b0-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="978b0-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="978b0-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="978b0-117">備註</span><span class="sxs-lookup"><span data-stu-id="978b0-117">Remarks</span></span>

<span data-ttu-id="978b0-118">這個介面和方法是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="978b0-118">This interface and method were introduced in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="978b0-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="978b0-119">Requirements</span></span>



| <span data-ttu-id="978b0-120">需求</span><span class="sxs-lookup"><span data-stu-id="978b0-120">Requirement</span></span> | <span data-ttu-id="978b0-121">值</span><span class="sxs-lookup"><span data-stu-id="978b0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="978b0-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="978b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="978b0-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="978b0-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="978b0-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="978b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="978b0-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="978b0-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="978b0-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="978b0-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="978b0-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="978b0-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="978b0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="978b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978b0-129">**ITablet2 介面**</span><span class="sxs-lookup"><span data-stu-id="978b0-129">**ITablet2 Interface**</span></span>](itablet2.md)
</dt> <dt>

[<span data-ttu-id="978b0-130">**平板電腦 \_ 裝置 \_ 種類列舉**</span><span class="sxs-lookup"><span data-stu-id="978b0-130">**TABLET\_DEVICE\_KIND Enumeration**</span></span>](tablet-device-kind.md)
</dt> <dt>

[<span data-ttu-id="978b0-131">**ITablet 介面**</span><span class="sxs-lookup"><span data-stu-id="978b0-131">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




