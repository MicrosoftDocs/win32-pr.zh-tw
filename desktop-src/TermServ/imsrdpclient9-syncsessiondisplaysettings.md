---
title: IMsRdpClient9 SyncSessionDisplaySettings 方法
description: 同步處理會話顯示設定。
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- SyncSessionDisplaySettings 方法遠端桌面服務
- SyncSessionDisplaySettings 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SyncSessionDisplaySettings 方法
- SyncSessionDisplaySettings 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，SyncSessionDisplaySettings 方法
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933932"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a><span data-ttu-id="41c98-108">IMsRdpClient9：： SyncSessionDisplaySettings 方法</span><span class="sxs-lookup"><span data-stu-id="41c98-108">IMsRdpClient9::SyncSessionDisplaySettings method</span></span>

<span data-ttu-id="41c98-109">同步處理會話顯示設定。</span><span class="sxs-lookup"><span data-stu-id="41c98-109">Synchronizes session display settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c98-110">語法</span><span class="sxs-lookup"><span data-stu-id="41c98-110">Syntax</span></span>


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a><span data-ttu-id="41c98-111">參數</span><span class="sxs-lookup"><span data-stu-id="41c98-111">Parameters</span></span>

<span data-ttu-id="41c98-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="41c98-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41c98-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="41c98-113">Return value</span></span>

<span data-ttu-id="41c98-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="41c98-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41c98-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="41c98-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c98-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="41c98-116">Requirements</span></span>



| <span data-ttu-id="41c98-117">需求</span><span class="sxs-lookup"><span data-stu-id="41c98-117">Requirement</span></span> | <span data-ttu-id="41c98-118">值</span><span class="sxs-lookup"><span data-stu-id="41c98-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c98-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41c98-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41c98-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41c98-120">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="41c98-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41c98-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41c98-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="41c98-122">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="41c98-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="41c98-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="41c98-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c98-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="41c98-125">DLL</span><span class="sxs-lookup"><span data-stu-id="41c98-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c98-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c98-126"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="41c98-127">IID</span><span class="sxs-lookup"><span data-stu-id="41c98-127">IID</span></span><br/>                      | <span data-ttu-id="41c98-128">CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="41c98-128">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="41c98-129">CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="41c98-129">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="41c98-130">IID \_ IMsRdpClient9 定義為28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="41c98-130">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41c98-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41c98-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c98-132">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="41c98-132">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="41c98-133">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="41c98-133">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





