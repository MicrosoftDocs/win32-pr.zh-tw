---
title: IMsTscAxEvents OnServiceMessageReceived 方法
description: 當用戶端收到系統訊息時呼叫。
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- OnServiceMessageReceived 方法遠端桌面服務
- OnServiceMessageReceived 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnServiceMessageReceived 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686055"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a><span data-ttu-id="7a69d-106">IMsTscAxEvents：： OnServiceMessageReceived 方法</span><span class="sxs-lookup"><span data-stu-id="7a69d-106">IMsTscAxEvents::OnServiceMessageReceived method</span></span>

<span data-ttu-id="7a69d-107">當用戶端收到系統訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a69d-107">Called when the client receives a system message.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a69d-108">語法</span><span class="sxs-lookup"><span data-stu-id="7a69d-108">Syntax</span></span>


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a><span data-ttu-id="7a69d-109">參數</span><span class="sxs-lookup"><span data-stu-id="7a69d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a69d-110">*serviceMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a69d-110">*serviceMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a69d-111">指定系統訊息。</span><span class="sxs-lookup"><span data-stu-id="7a69d-111">Specifies the system message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a69d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a69d-112">Return value</span></span>

<span data-ttu-id="7a69d-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7a69d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a69d-114">備註</span><span class="sxs-lookup"><span data-stu-id="7a69d-114">Remarks</span></span>

<span data-ttu-id="7a69d-115">如需系統訊息的詳細資訊，請參閱 [設定遠端桌面閘道伺服器的訊息](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="7a69d-115">For more information about system messages, see [Configure Messaging for a Remote Desktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a69d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a69d-116">Requirements</span></span>



| <span data-ttu-id="7a69d-117">需求</span><span class="sxs-lookup"><span data-stu-id="7a69d-117">Requirement</span></span> | <span data-ttu-id="7a69d-118">值</span><span class="sxs-lookup"><span data-stu-id="7a69d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a69d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a69d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a69d-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a69d-120">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="7a69d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a69d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a69d-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a69d-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="7a69d-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7a69d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a69d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a69d-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a69d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7a69d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a69d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a69d-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a69d-127">IID</span><span class="sxs-lookup"><span data-stu-id="7a69d-127">IID</span></span><br/>                      | <span data-ttu-id="7a69d-128">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="7a69d-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7a69d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a69d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a69d-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="7a69d-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

