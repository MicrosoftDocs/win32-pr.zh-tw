---
title: IMsTscAxEvents OnLoginComplete 方法
description: 當用戶端控制項成功登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時呼叫，並遵循 Windows 登入對話方塊的顯示。
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- OnLoginComplete 方法遠端桌面服務
- OnLoginComplete 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnLoginComplete 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508760"
---
# <a name="imstscaxeventsonlogincomplete-method"></a><span data-ttu-id="edf63-106">IMsTscAxEvents：： OnLoginComplete 方法</span><span class="sxs-lookup"><span data-stu-id="edf63-106">IMsTscAxEvents::OnLoginComplete method</span></span>

<span data-ttu-id="edf63-107">當用戶端控制項成功登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時呼叫，並遵循 Windows 登入對話方塊的顯示。</span><span class="sxs-lookup"><span data-stu-id="edf63-107">Called when the client control has successfully logged on to a Remote Desktop Session Host (RD Session Host) server, following the display of the Windows Logon dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="edf63-108">語法</span><span class="sxs-lookup"><span data-stu-id="edf63-108">Syntax</span></span>


```C++
void OnLoginComplete();
```



## <a name="parameters"></a><span data-ttu-id="edf63-109">參數</span><span class="sxs-lookup"><span data-stu-id="edf63-109">Parameters</span></span>

<span data-ttu-id="edf63-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="edf63-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edf63-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="edf63-111">Return value</span></span>

<span data-ttu-id="edf63-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="edf63-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edf63-113">備註</span><span class="sxs-lookup"><span data-stu-id="edf63-113">Remarks</span></span>

<span data-ttu-id="edf63-114">在事件接收中執行此方法，以接收控制項已完成登入的通知。</span><span class="sxs-lookup"><span data-stu-id="edf63-114">Implement this method in your event sink to receive notification that the control has completed logon.</span></span>

## <a name="examples"></a><span data-ttu-id="edf63-115">範例</span><span class="sxs-lookup"><span data-stu-id="edf63-115">Examples</span></span>

<span data-ttu-id="edf63-116">下列範例示範如何使用 Visual Basic 腳本處理常式代碼來處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="edf63-116">The following example shows how to handle this event by using Visual Basic Scripting code.</span></span> <span data-ttu-id="edf63-117">此範例中的假設是您的控制項物件名稱為 "MsRdpClient"。</span><span class="sxs-lookup"><span data-stu-id="edf63-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="edf63-118">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="edf63-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a><span data-ttu-id="edf63-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="edf63-119">Requirements</span></span>



| <span data-ttu-id="edf63-120">需求</span><span class="sxs-lookup"><span data-stu-id="edf63-120">Requirement</span></span> | <span data-ttu-id="edf63-121">值</span><span class="sxs-lookup"><span data-stu-id="edf63-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edf63-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edf63-122">Minimum supported client</span></span><br/> | <span data-ttu-id="edf63-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edf63-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="edf63-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edf63-124">Minimum supported server</span></span><br/> | <span data-ttu-id="edf63-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edf63-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="edf63-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="edf63-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="edf63-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edf63-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="edf63-128">DLL</span><span class="sxs-lookup"><span data-stu-id="edf63-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edf63-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edf63-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="edf63-130">IID</span><span class="sxs-lookup"><span data-stu-id="edf63-130">IID</span></span><br/>                      | <span data-ttu-id="edf63-131">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="edf63-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="edf63-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edf63-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf63-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="edf63-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





