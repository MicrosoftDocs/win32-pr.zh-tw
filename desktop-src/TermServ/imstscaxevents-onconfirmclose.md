---
title: IMsTscAxEvents OnConfirmClose 方法
description: 當用戶端呼叫 IMsRdpClient RequestClose 方法時呼叫。
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- OnConfirmClose 方法遠端桌面服務
- OnConfirmClose 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnConfirmClose 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106487"
---
# <a name="imstscaxeventsonconfirmclose-method"></a><span data-ttu-id="9644c-106">IMsTscAxEvents：： OnConfirmClose 方法</span><span class="sxs-lookup"><span data-stu-id="9644c-106">IMsTscAxEvents::OnConfirmClose method</span></span>

<span data-ttu-id="9644c-107">當用戶端呼叫 [**IMsRdpClient：： RequestClose**](imsrdpclient-requestclose.md) 方法時呼叫。</span><span class="sxs-lookup"><span data-stu-id="9644c-107">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span> <span data-ttu-id="9644c-108">為了回應此事件，系統應該會提示使用者確認關閉連接。</span><span class="sxs-lookup"><span data-stu-id="9644c-108">In response to this event, the user should be prompted to confirm closing the connection.</span></span> <span data-ttu-id="9644c-109">如需詳細資訊，請參閱接下來的＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="9644c-109">For more information, see the following Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="9644c-110">語法</span><span class="sxs-lookup"><span data-stu-id="9644c-110">Syntax</span></span>


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a><span data-ttu-id="9644c-111">參數</span><span class="sxs-lookup"><span data-stu-id="9644c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9644c-112">*pfAllowClose* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9644c-112">*pfAllowClose* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9644c-113">如果 **VARIANT \_ TRUE**（預設值）表示使用者想要關閉連接。</span><span class="sxs-lookup"><span data-stu-id="9644c-113">If **VARIANT\_TRUE**, the default, indicates that the user wants to close the connection.</span></span> <span data-ttu-id="9644c-114">如果 **VARIANT \_ FALSE**，表示使用者不想關閉連接。</span><span class="sxs-lookup"><span data-stu-id="9644c-114">If **VARIANT\_FALSE**, indicates that the user does not want to close the connection.</span></span> <span data-ttu-id="9644c-115">如需詳細資訊，請參閱接下來的＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="9644c-115">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9644c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9644c-116">Return value</span></span>

<span data-ttu-id="9644c-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9644c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9644c-118">備註</span><span class="sxs-lookup"><span data-stu-id="9644c-118">Remarks</span></span>

<span data-ttu-id="9644c-119">當容器應用程式呼叫 [**IMsRdpClient：： RequestClose**](imsrdpclient-requestclose.md) 方法時，該方法會傳回一個值，指出容器是否應該在關閉控制項連接之前等候 **OnConfirmClose** 事件。</span><span class="sxs-lookup"><span data-stu-id="9644c-119">When a container application calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method, that method returns a value indicating whether the container should wait for an **OnConfirmClose** event to occur before closing the control connection.</span></span> <span data-ttu-id="9644c-120">如果 **RequestClose** 傳回 **controlCloseWaitForEvents**，而且使用者已連接並登入遠端桌面服務會話，則會引發 **OnConfirmClose** 事件。</span><span class="sxs-lookup"><span data-stu-id="9644c-120">If **RequestClose** returns **controlCloseWaitForEvents**, and the user is connected and logged on to their Remote Desktop Services session, the **OnConfirmClose** event fires.</span></span> <span data-ttu-id="9644c-121">屆時，容器應用程式可以提示使用者，詢問使用者是否想要關閉連接。</span><span class="sxs-lookup"><span data-stu-id="9644c-121">At that point the container application can prompt the user, asking whether the user wants to close the connection.</span></span> <span data-ttu-id="9644c-122">如果使用者想要關閉連接，應用程式應該將 *pfAllowClose* 參數設定為 **VARIANT \_ TRUE** ，然後繼續關閉連接。</span><span class="sxs-lookup"><span data-stu-id="9644c-122">If the user wants to close the connection, the application should set the *pfAllowClose* parameter to **VARIANT\_TRUE** and proceed with closing the connection.</span></span> <span data-ttu-id="9644c-123">如果使用者不想要關閉，應用程式應該將 *pfAllowClose* 設定為 **VARIANT \_ FALSE** ，並讓連接保持開啟。</span><span class="sxs-lookup"><span data-stu-id="9644c-123">If the user does not want to close, the application should set *pfAllowClose* to **VARIANT\_FALSE** and leave the connection open.</span></span>

<span data-ttu-id="9644c-124">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="9644c-124">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9644c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9644c-125">Requirements</span></span>



| <span data-ttu-id="9644c-126">需求</span><span class="sxs-lookup"><span data-stu-id="9644c-126">Requirement</span></span> | <span data-ttu-id="9644c-127">值</span><span class="sxs-lookup"><span data-stu-id="9644c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9644c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9644c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9644c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9644c-129">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9644c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9644c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9644c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9644c-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9644c-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9644c-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="9644c-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9644c-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9644c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9644c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9644c-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9644c-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9644c-136">IID</span><span class="sxs-lookup"><span data-stu-id="9644c-136">IID</span></span><br/>                      | <span data-ttu-id="9644c-137">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9644c-137">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9644c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9644c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9644c-139">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9644c-139">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





