---
description: 手寫筆提示接觸到數位化的平板電腦介面時發生。
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: ITabletEventSink：： CursorDown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693344"
---
# <a name="itableteventsinkcursordown-method"></a><span data-ttu-id="047fb-103">ITabletEventSink：： CursorDown 方法</span><span class="sxs-lookup"><span data-stu-id="047fb-103">ITabletEventSink::CursorDown method</span></span>

<span data-ttu-id="047fb-104">手寫筆提示接觸到數位化的平板電腦介面時發生。</span><span class="sxs-lookup"><span data-stu-id="047fb-104">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="047fb-105">語法</span><span class="sxs-lookup"><span data-stu-id="047fb-105">Syntax</span></span>


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="047fb-106">參數</span><span class="sxs-lookup"><span data-stu-id="047fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="047fb-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="047fb-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="047fb-108">Tablet 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="047fb-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="047fb-109"> \[ 中的 cid\]</span><span class="sxs-lookup"><span data-stu-id="047fb-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="047fb-110">手寫筆的識別碼。</span><span class="sxs-lookup"><span data-stu-id="047fb-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="047fb-111">*nSerialNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="047fb-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="047fb-112">手寫筆的序號。</span><span class="sxs-lookup"><span data-stu-id="047fb-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="047fb-113">*cbPkt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="047fb-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="047fb-114">手寫筆資料封包中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="047fb-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="047fb-115">*pbPkt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="047fb-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="047fb-116">手寫筆資料，指出手寫筆接觸 tablet 的位置。</span><span class="sxs-lookup"><span data-stu-id="047fb-116">The stylus data indicating the location where the stylus touched the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="047fb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="047fb-117">Return value</span></span>

<span data-ttu-id="047fb-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="047fb-118">This method can return one of these values.</span></span>



| <span data-ttu-id="047fb-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="047fb-119">Return code</span></span>                                                                            | <span data-ttu-id="047fb-120">Description</span><span class="sxs-lookup"><span data-stu-id="047fb-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="047fb-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="047fb-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="047fb-122">成功。</span><span class="sxs-lookup"><span data-stu-id="047fb-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="047fb-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="047fb-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="047fb-124">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="047fb-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="047fb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="047fb-125">Requirements</span></span>



| <span data-ttu-id="047fb-126">需求</span><span class="sxs-lookup"><span data-stu-id="047fb-126">Requirement</span></span> | <span data-ttu-id="047fb-127">值</span><span class="sxs-lookup"><span data-stu-id="047fb-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="047fb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="047fb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="047fb-129">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="047fb-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="047fb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="047fb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="047fb-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="047fb-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="047fb-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="047fb-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="047fb-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="047fb-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047fb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="047fb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047fb-135">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="047fb-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




