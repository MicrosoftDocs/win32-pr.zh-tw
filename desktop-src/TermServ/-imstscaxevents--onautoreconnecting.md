---
title: IMsTscAxEvents OnAutoReconnecting 方法
description: 當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。 |IMsTscAxEvents OnAutoReconnecting 方法
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting 方法遠端桌面服務
- OnAutoReconnecting 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAutoReconnecting 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322371"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a><span data-ttu-id="d301c-107">IMsTscAxEvents：： OnAutoReconnecting 方法</span><span class="sxs-lookup"><span data-stu-id="d301c-107">IMsTscAxEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="d301c-108">當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="d301c-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d301c-109">語法</span><span class="sxs-lookup"><span data-stu-id="d301c-109">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d301c-110">參數</span><span class="sxs-lookup"><span data-stu-id="d301c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d301c-111">*disconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d301c-111">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d301c-112">描述上次會話中斷連接原因的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d301c-112">Code describing the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="d301c-113">*了 attemptcount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d301c-113">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d301c-114">目前自動重新連接程式中所做的嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="d301c-114">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="d301c-115">每次嘗試時，此計數都會增加一個。</span><span class="sxs-lookup"><span data-stu-id="d301c-115">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="d301c-116">*pArcContinueStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d301c-116">*pArcContinueStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d301c-117">傳回的程式碼指標，指定自動重新連接程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="d301c-117">Pointer to a returned code specifying the state of the automatic reconnection process.</span></span> <span data-ttu-id="d301c-118">您可以重設此程式碼，以變更目前自動重新連接程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="d301c-118">This code can be reset to change the state of the current automatic reconnection process.</span></span>

<span data-ttu-id="d301c-119">如需重設此程式碼的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="d301c-119">For more information about resetting this code, refer to the Remarks section.</span></span>

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span data-ttu-id="d301c-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic \* \* \* (0) </span><span class="sxs-lookup"><span data-stu-id="d301c-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>\*\*\*\*autoReconnectContinueAutomatic\*\*\*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="d301c-121">重新連接程式會自動發生。</span><span class="sxs-lookup"><span data-stu-id="d301c-121">The reconnection process is occurring automatically.</span></span> <span data-ttu-id="d301c-122">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="d301c-122">This is the default value.</span></span>

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span data-ttu-id="d301c-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop \* \* \* (1) </span><span class="sxs-lookup"><span data-stu-id="d301c-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>\*\*\*\*autoReconnectContinueStop\*\*\*\* (1)</span></span>


</dt> <dd>

<span data-ttu-id="d301c-124">重新連接程式已停止。</span><span class="sxs-lookup"><span data-stu-id="d301c-124">The reconnection process has been stopped.</span></span>

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span data-ttu-id="d301c-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual \* \* \* (2) </span><span class="sxs-lookup"><span data-stu-id="d301c-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>\*\*\*\*autoReconnectContinueManual\*\*\*\* (2)</span></span>


</dt> <dd>

<span data-ttu-id="d301c-126">重新連接程式是以手動方式發生。</span><span class="sxs-lookup"><span data-stu-id="d301c-126">The reconnection process is occurring manually.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d301c-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="d301c-127">Return value</span></span>

<span data-ttu-id="d301c-128">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d301c-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d301c-129">備註</span><span class="sxs-lookup"><span data-stu-id="d301c-129">Remarks</span></span>

<span data-ttu-id="d301c-130">在事件接收中執行此方法，以接收控制項重新建立與 RD 工作階段主機伺服器之連接的通知。</span><span class="sxs-lookup"><span data-stu-id="d301c-130">Implement this method in your event sink to receive notification that the control is reestablishing a connection with an RD Session Host server.</span></span>

<span data-ttu-id="d301c-131">如果透過將 *pArcContinueStatus* 參數的值設定為 **autoReconnectContinueAutomatic** 來變更自動重新連線程式的狀態，這個方法就會以純粹的諮詢模式來運作。</span><span class="sxs-lookup"><span data-stu-id="d301c-131">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueAutomatic**, this method functions in a purely advisory mode.</span></span> <span data-ttu-id="d301c-132">容器可以接聽此事件，以取得自動重新連接程式正在進行的通知。</span><span class="sxs-lookup"><span data-stu-id="d301c-132">Containers can listen to this event for notifications that the automatic reconnection process is proceeding.</span></span> <span data-ttu-id="d301c-133">控制項將會根據自己的內部時間和嘗試計數，自動繼續嘗試重新建立連接。</span><span class="sxs-lookup"><span data-stu-id="d301c-133">The control will automatically keep trying to re-establish a connection based on its own internal timing and attempt counts.</span></span> <span data-ttu-id="d301c-134">在每次自動重新連線嘗試期間都會呼叫這個方法，以便通知容器。</span><span class="sxs-lookup"><span data-stu-id="d301c-134">This method is called during each automatic reconnection attempt in order to notify the container.</span></span>

<span data-ttu-id="d301c-135">將 *pArcContinueStatus* 參數的值設定為 **autoReconnectContinueStop** 時，自動重新連接程式的狀態變更時，將會終止目前的自動重新連線嘗試，並將中斷連線通知傳送至容器，而不會再發出任何自動重新連線通知。</span><span class="sxs-lookup"><span data-stu-id="d301c-135">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueStop**, the current automatic reconnection attempt will be terminated, a disconnect notification will be sent to the container, and no further automatic reconnect notifications will be issued.</span></span>

> [!Note]  
> <span data-ttu-id="d301c-136">使用 [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) 屬性來啟用或停用自動重新連接。</span><span class="sxs-lookup"><span data-stu-id="d301c-136">Use the [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) property to enable or disable automatic reconnection.</span></span>

 

<span data-ttu-id="d301c-137">透過將 *pArcContinueStatus* 參數的值設定為 **autoReconnectContinueManual** 來變更自動重新連線程式的狀態時，容器將會藉由呼叫 [**Connect**](imstscax-connect.md) 來觸發連接嘗試或 [**中斷**](imstscax-disconnect.md) 連線以取消自動重新連線程式，以手動方式控制自動重新連接程式。</span><span class="sxs-lookup"><span data-stu-id="d301c-137">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueManual**, the container will manually control the automatic reconnection process by calling [**Connect**](imstscax-connect.md) to trigger a connection attempt or [**Disconnect**](imstscax-disconnect.md) to cancel the automatic reconnection process.</span></span> <span data-ttu-id="d301c-138">一旦設定為此值，控制項就會停止進行自動重新連線嘗試，並成為容器的原則，以進行 **連接** 呼叫以觸發自動重新連線嘗試。</span><span class="sxs-lookup"><span data-stu-id="d301c-138">Once set to this value, the control will stop making automatic reconnection attempts and it becomes the policy of the container to make **Connect** calls to trigger automatic reconnection attempts.</span></span> <span data-ttu-id="d301c-139">這是在容器提供自動重新連線的自訂 UI 行為時完成，例如在自動重新連線程式之前重新開機已中斷的 RAS 或 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="d301c-139">This is done when the container provides customized UI behavior for automatic reconnection, such as restarting a dropped RAS or VPN connection before the automatic reconnection process.</span></span>

<span data-ttu-id="d301c-140">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="d301c-140">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d301c-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="d301c-141">Requirements</span></span>



| <span data-ttu-id="d301c-142">需求</span><span class="sxs-lookup"><span data-stu-id="d301c-142">Requirement</span></span> | <span data-ttu-id="d301c-143">值</span><span class="sxs-lookup"><span data-stu-id="d301c-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d301c-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d301c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d301c-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d301c-145">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d301c-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d301c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d301c-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d301c-147">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d301c-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d301c-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="d301c-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d301c-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d301c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d301c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d301c-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d301c-151"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d301c-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d301c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d301c-153">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="d301c-153">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





