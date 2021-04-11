---
description: 手寫筆在數位板上移動時發生。
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink：:P ackets 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944673"
---
# <a name="itableteventsinkpackets-method"></a><span data-ttu-id="adce4-103">ITabletEventSink：:P ackets 方法</span><span class="sxs-lookup"><span data-stu-id="adce4-103">ITabletEventSink::Packets method</span></span>

<span data-ttu-id="adce4-104">手寫筆在數位板上移動時發生。</span><span class="sxs-lookup"><span data-stu-id="adce4-104">Occurs when the stylus is moving on the digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="adce4-105">語法</span><span class="sxs-lookup"><span data-stu-id="adce4-105">Syntax</span></span>


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="adce4-106">參數</span><span class="sxs-lookup"><span data-stu-id="adce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adce4-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adce4-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adce4-108">Tablet 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="adce4-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="adce4-109">*cPkts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adce4-109">*cPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adce4-110">封包數目。</span><span class="sxs-lookup"><span data-stu-id="adce4-110">The number of packets.</span></span>

</dd> <dt>

<span data-ttu-id="adce4-111">*cbPkts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adce4-111">*cbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adce4-112">封包緩衝區的大小</span><span class="sxs-lookup"><span data-stu-id="adce4-112">The size of packet buffer</span></span>

</dd> <dt>

<span data-ttu-id="adce4-113">*pbPkts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adce4-113">*pbPkts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adce4-114">封包緩衝區。</span><span class="sxs-lookup"><span data-stu-id="adce4-114">The packet buffer.</span></span>

</dd> <dt>

<span data-ttu-id="adce4-115">*pnSerialNumbers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adce4-115">*pnSerialNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adce4-116">序號陣列。</span><span class="sxs-lookup"><span data-stu-id="adce4-116">The serial number array.</span></span>

</dd> <dt>

<span data-ttu-id="adce4-117">*Cid*</span><span class="sxs-lookup"><span data-stu-id="adce4-117">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="adce4-118">手寫筆的識別碼。</span><span class="sxs-lookup"><span data-stu-id="adce4-118">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adce4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="adce4-119">Return value</span></span>

<span data-ttu-id="adce4-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="adce4-120">This method can return one of these values.</span></span>



| <span data-ttu-id="adce4-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="adce4-121">Return code</span></span>                                                                            | <span data-ttu-id="adce4-122">Description</span><span class="sxs-lookup"><span data-stu-id="adce4-122">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="adce4-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="adce4-123"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="adce4-124">成功。</span><span class="sxs-lookup"><span data-stu-id="adce4-124">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="adce4-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="adce4-125"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="adce4-126">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="adce4-126">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="adce4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="adce4-127">Requirements</span></span>



| <span data-ttu-id="adce4-128">需求</span><span class="sxs-lookup"><span data-stu-id="adce4-128">Requirement</span></span> | <span data-ttu-id="adce4-129">值</span><span class="sxs-lookup"><span data-stu-id="adce4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adce4-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adce4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="adce4-131">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adce4-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="adce4-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adce4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="adce4-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="adce4-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="adce4-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="adce4-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="adce4-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="adce4-135"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adce4-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adce4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adce4-137">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="adce4-137">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




