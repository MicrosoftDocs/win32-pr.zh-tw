---
description: 發生于使用者從 tablet 數位板介面引發手寫筆時。
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: ITabletEventSink：： CursorUp 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195112"
---
# <a name="itableteventsinkcursorup-method"></a><span data-ttu-id="3e2ab-103">ITabletEventSink：： CursorUp 方法</span><span class="sxs-lookup"><span data-stu-id="3e2ab-103">ITabletEventSink::CursorUp method</span></span>

<span data-ttu-id="3e2ab-104">發生于使用者從 tablet 數位板介面引發手寫筆時。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-104">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e2ab-105">Syntax</span></span>


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="3e2ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e2ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e2ab-107">*tcid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e2ab-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2ab-108">Tablet 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="3e2ab-109"> \[ 中的 cid\]</span><span class="sxs-lookup"><span data-stu-id="3e2ab-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2ab-110">手寫筆的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="3e2ab-111">*nSerialNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e2ab-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2ab-112">手寫筆的序號。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="3e2ab-113">*cbPkt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e2ab-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2ab-114">手寫筆資料封包中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="3e2ab-115">*pbPkt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e2ab-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2ab-116">手寫筆資料，指出手寫筆從平板電腦中提起的位置。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-116">The stylus data indicating the location where the stylus was lifted from the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e2ab-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e2ab-117">Return value</span></span>

<span data-ttu-id="3e2ab-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e2ab-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3e2ab-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e2ab-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e2ab-120">Requirements</span></span>



| <span data-ttu-id="3e2ab-121">需求</span><span class="sxs-lookup"><span data-stu-id="3e2ab-121">Requirement</span></span> | <span data-ttu-id="3e2ab-122">值</span><span class="sxs-lookup"><span data-stu-id="3e2ab-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2ab-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e2ab-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2ab-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e2ab-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3e2ab-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e2ab-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2ab-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e2ab-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3e2ab-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e2ab-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e2ab-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e2ab-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e2ab-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e2ab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2ab-130">**ITabletEventSink 介面**</span><span class="sxs-lookup"><span data-stu-id="3e2ab-130">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




