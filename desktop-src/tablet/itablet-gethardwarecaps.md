---
description: 傳回值，這個值表示平板電腦硬體的功能。
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: ITablet：： GetHardwareCaps 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851607"
---
# <a name="itabletgethardwarecaps-method"></a><span data-ttu-id="c3343-103">ITablet：： GetHardwareCaps 方法</span><span class="sxs-lookup"><span data-stu-id="c3343-103">ITablet::GetHardwareCaps method</span></span>

<span data-ttu-id="c3343-104">傳回值，這個值表示平板電腦硬體的功能。</span><span class="sxs-lookup"><span data-stu-id="c3343-104">Returns a value that represents the capabilities of the tablet hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3343-105">語法</span><span class="sxs-lookup"><span data-stu-id="c3343-105">Syntax</span></span>


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a><span data-ttu-id="c3343-106">參數</span><span class="sxs-lookup"><span data-stu-id="c3343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3343-107">*pdwCaps* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3343-107">*pdwCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3343-108">代表平板電腦硬體功能的位旗標。</span><span class="sxs-lookup"><span data-stu-id="c3343-108">Bit flags that represent the capabilities of the tablet hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3343-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3343-109">Return value</span></span>

<span data-ttu-id="c3343-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c3343-110">This method can return one of these values.</span></span>



| <span data-ttu-id="c3343-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c3343-111">Return code</span></span>                                                                            | <span data-ttu-id="c3343-112">Description</span><span class="sxs-lookup"><span data-stu-id="c3343-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c3343-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c3343-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="c3343-114">成功。</span><span class="sxs-lookup"><span data-stu-id="c3343-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="c3343-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="c3343-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="c3343-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3343-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3343-117">備註</span><span class="sxs-lookup"><span data-stu-id="c3343-117">Remarks</span></span>

<span data-ttu-id="c3343-118">*PdwCaps* 參數是一組用來描述平板電腦硬體功能的位旗標。</span><span class="sxs-lookup"><span data-stu-id="c3343-118">The *pdwCaps* parameter is a set of bit flags that describe tablet hardware capabilities.</span></span> <span data-ttu-id="c3343-119">下表描述這些旗標。</span><span class="sxs-lookup"><span data-stu-id="c3343-119">The following table describes these flags.</span></span>



| <span data-ttu-id="c3343-120">旗標名稱</span><span class="sxs-lookup"><span data-stu-id="c3343-120">Flag Name</span></span>                         | <span data-ttu-id="c3343-121">值</span><span class="sxs-lookup"><span data-stu-id="c3343-121">Value</span></span>                 | <span data-ttu-id="c3343-122">描述</span><span class="sxs-lookup"><span data-stu-id="c3343-122">Description</span></span>                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3343-123">THWC \_ 整合式</span><span class="sxs-lookup"><span data-stu-id="c3343-123">THWC\_INTEGRATED</span></span><br/>       | <span data-ttu-id="c3343-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3343-124">0x00000001</span></span><br/> | <span data-ttu-id="c3343-125">指出顯示器和數位板會共用相同的表面。</span><span class="sxs-lookup"><span data-stu-id="c3343-125">Indicates that the display and digitizer share the same surface.</span></span><br/>                                                    |
| <span data-ttu-id="c3343-126">THWC \_ CSR \_ 必須 \_ 接觸</span><span class="sxs-lookup"><span data-stu-id="c3343-126">THWC\_CSR\_MUST\_TOUCH</span></span><br/> | <span data-ttu-id="c3343-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c3343-127">0x00000002</span></span><br/> | <span data-ttu-id="c3343-128">表示資料指標必須在與裝置的實體連絡人之間，才能報告位置。</span><span class="sxs-lookup"><span data-stu-id="c3343-128">Indicates that the cursor must be in physical contact with the device to report position.</span></span><br/>                           |
| <span data-ttu-id="c3343-129">THWC \_ 硬 \_ 距離</span><span class="sxs-lookup"><span data-stu-id="c3343-129">THWC\_HARD\_PROXIMITY</span></span><br/>  | <span data-ttu-id="c3343-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c3343-130">0x00000004</span></span><br/> | <span data-ttu-id="c3343-131">指出當游標進入並離開實體偵測範圍時，裝置可以產生事件。</span><span class="sxs-lookup"><span data-stu-id="c3343-131">Indicates that the device can generate events when the cursor is entering and leaving the physical detection range.</span></span><br/> |
| <span data-ttu-id="c3343-132">THWC \_ PHYSID \_ CSR</span><span class="sxs-lookup"><span data-stu-id="c3343-132">THWC\_PHYSID\_CSRS</span></span><br/>     | <span data-ttu-id="c3343-133">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c3343-133">0x00000008</span></span><br/> | <span data-ttu-id="c3343-134">指出裝置可在硬體中唯一識別作用中的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c3343-134">Indicates that the device can uniquely identify the active cursor in hardware.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="c3343-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3343-135">Requirements</span></span>



| <span data-ttu-id="c3343-136">需求</span><span class="sxs-lookup"><span data-stu-id="c3343-136">Requirement</span></span> | <span data-ttu-id="c3343-137">值</span><span class="sxs-lookup"><span data-stu-id="c3343-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3343-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3343-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c3343-139">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3343-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c3343-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3343-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c3343-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="c3343-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c3343-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3343-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3343-143"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3343-143"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3343-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3343-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3343-145">**ITablet 介面**</span><span class="sxs-lookup"><span data-stu-id="c3343-145">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




