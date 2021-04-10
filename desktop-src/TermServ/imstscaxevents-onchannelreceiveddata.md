---
title: IMsTscAxEvents OnChannelReceivedData 方法
description: 當用戶端在可編寫腳本的虛擬通道上接收資料時呼叫。
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- OnChannelReceivedData 方法遠端桌面服務
- OnChannelReceivedData 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnChannelReceivedData 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094472"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a><span data-ttu-id="a38eb-106">IMsTscAxEvents：： OnChannelReceivedData 方法</span><span class="sxs-lookup"><span data-stu-id="a38eb-106">IMsTscAxEvents::OnChannelReceivedData method</span></span>

<span data-ttu-id="a38eb-107">當用戶端在可編寫腳本的虛擬通道上接收資料時呼叫。</span><span class="sxs-lookup"><span data-stu-id="a38eb-107">Called when the client receives data on a scriptable virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38eb-108">語法</span><span class="sxs-lookup"><span data-stu-id="a38eb-108">Syntax</span></span>


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a><span data-ttu-id="a38eb-109">參數</span><span class="sxs-lookup"><span data-stu-id="a38eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38eb-110">*chanName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a38eb-110">*chanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38eb-111">收到資料的虛擬通道名稱。</span><span class="sxs-lookup"><span data-stu-id="a38eb-111">The name of the virtual channel on which data was received.</span></span> <span data-ttu-id="a38eb-112">這個名稱符合對 [**IMsTscAx：： CreateVirtualChannels**](imstscax-createvirtualchannels.md)的呼叫所建立的其中一個通道。</span><span class="sxs-lookup"><span data-stu-id="a38eb-112">This name matches one of the channels created by the call to [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38eb-113">*資料* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a38eb-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38eb-114">在可編寫腳本的虛擬通道上收到的資料。</span><span class="sxs-lookup"><span data-stu-id="a38eb-114">The data received on the scriptable virtual channel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38eb-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a38eb-115">Return value</span></span>

<span data-ttu-id="a38eb-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a38eb-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a38eb-117">備註</span><span class="sxs-lookup"><span data-stu-id="a38eb-117">Remarks</span></span>

<span data-ttu-id="a38eb-118">如需此事件的詳細資訊，請參閱 [使用遠端桌面網頁連線執行可編寫腳本的虛擬通道](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) 。</span><span class="sxs-lookup"><span data-stu-id="a38eb-118">Refer to [Implementing Scriptable Virtual Channels using Remote Desktop Web Connection](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) for more information about this event.</span></span>

<span data-ttu-id="a38eb-119">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="a38eb-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a38eb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a38eb-120">Requirements</span></span>



| <span data-ttu-id="a38eb-121">需求</span><span class="sxs-lookup"><span data-stu-id="a38eb-121">Requirement</span></span> | <span data-ttu-id="a38eb-122">值</span><span class="sxs-lookup"><span data-stu-id="a38eb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a38eb-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a38eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a38eb-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a38eb-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a38eb-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a38eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a38eb-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a38eb-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a38eb-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a38eb-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a38eb-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a38eb-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a38eb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a38eb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a38eb-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a38eb-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a38eb-131">IID</span><span class="sxs-lookup"><span data-stu-id="a38eb-131">IID</span></span><br/>                      | <span data-ttu-id="a38eb-132">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="a38eb-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a38eb-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a38eb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38eb-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="a38eb-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





