---
description: 感應器 API 提供的方法可用來提示使用者使用感應器或感應器集合的許可權。
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: 管理使用者權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb65fa5a9962be4850aa4711cafa03fb7658212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943319"
---
# <a name="managing-user-permissions"></a><span data-ttu-id="af03d-103">管理使用者權限</span><span class="sxs-lookup"><span data-stu-id="af03d-103">Managing User Permissions</span></span>

<span data-ttu-id="af03d-104">感應器 API 提供的方法可用來提示使用者使用感應器或感應器集合的許可權。</span><span class="sxs-lookup"><span data-stu-id="af03d-104">The Sensor API provides a method you can use to prompt the user for permissions to use a sensor or collection of sensors.</span></span>

<span data-ttu-id="af03d-105">因為感應器可能會顯示機密資訊，所以 Windows 會要求使用者在您的程式可以存取任何資料之前，先啟用感應器。</span><span class="sxs-lookup"><span data-stu-id="af03d-105">Because sensors can reveal sensitive information, Windows requires that users enable sensors before your program can access any data.</span></span>

<span data-ttu-id="af03d-106">當您想要使用目前 [**SENSORSTATE**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) 感應器 \_ 狀態拒絕存取的感應器時，您可能會想要要求許可權 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="af03d-106">You may want to request permission when you want to use sensors for which the current [**SensorState**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) is SENSOR\_STATE\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="af03d-107">若要要求許可權，請呼叫 [**ISensorManager：： RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 方法。</span><span class="sxs-lookup"><span data-stu-id="af03d-107">To request permissions, call the [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) method.</span></span> <span data-ttu-id="af03d-108">當您呼叫這個方法時，Windows 會開啟 [ **啟用感應器** ] 對話方塊，提示使用者啟用您所要求的感應器。</span><span class="sxs-lookup"><span data-stu-id="af03d-108">When you call this method, Windows opens the **Enable sensors** dialog box to prompt the user to enable the sensors you requested.</span></span> <span data-ttu-id="af03d-109">此對話方塊會提供使用者您所要求之感應器的名稱。</span><span class="sxs-lookup"><span data-stu-id="af03d-109">This dialog box provides the user with the names of the sensors you requested.</span></span> <span data-ttu-id="af03d-110">使用者可以選擇下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="af03d-110">The user can choose one of the following options:</span></span>

-   <span data-ttu-id="af03d-111">**啟用這些感應器**。</span><span class="sxs-lookup"><span data-stu-id="af03d-111">**Enable these sensors**.</span></span>
-   <span data-ttu-id="af03d-112">**請勿啟用這些感應器**。</span><span class="sxs-lookup"><span data-stu-id="af03d-112">**Don't enable these sensors**.</span></span>
-   <span data-ttu-id="af03d-113">**開啟主控台以取得更多選項**。</span><span class="sxs-lookup"><span data-stu-id="af03d-113">**Open Control Panel for more options**.</span></span>

<span data-ttu-id="af03d-114">如果使用者選擇 [ **不啟用這些感應器**]，Windows 將不會再顯示那些特定感應器的 [ **啟用感應器** ] 對話方塊，即使您的程式呼叫 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)。</span><span class="sxs-lookup"><span data-stu-id="af03d-114">If a user chooses **Don't enable these sensors**, Windows will not show the **Enable sensors** dialog box again for those particular sensors, even if your program calls [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions).</span></span> <span data-ttu-id="af03d-115">如果使用者選擇任何其他選項，Windows 將允許在要求時顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="af03d-115">If the user chooses any other option, Windows will allow the dialog box to be displayed when requested.</span></span> <span data-ttu-id="af03d-116">如果您對 **RequestPermissions** 的呼叫包含某些使用者先前選擇要保持停用的感應器，感應器 API 將會從使用者看到的感應器清單中移除這些感應器。</span><span class="sxs-lookup"><span data-stu-id="af03d-116">If your call to **RequestPermissions** contains some sensors that the user has previously chosen to keep disabled, the Sensor API will remove these sensors from the list of sensors the user sees.</span></span>

### <a name="modal-or-modeless-behavior"></a><span data-ttu-id="af03d-117">強制回應或非模式行為</span><span class="sxs-lookup"><span data-stu-id="af03d-117">Modal or Modeless Behavior</span></span>

<span data-ttu-id="af03d-118">[**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)方法會使用 **布林值** 引數，判斷 [**啟用感應器**] 對話方塊是否顯示為強制回應或非強制回應視窗。</span><span class="sxs-lookup"><span data-stu-id="af03d-118">The [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) method takes a **Boolean** argument that determines whether the **Enable sensors** dialog box is displayed as a modal or modeless window.</span></span> <span data-ttu-id="af03d-119">這項設定也會影響對話方塊的行為是同步或非同步。</span><span class="sxs-lookup"><span data-stu-id="af03d-119">This setting also affects whether the behavior of the dialog box return code is synchronous or asynchronous.</span></span>

<span data-ttu-id="af03d-120">當強制回應時，對話方塊會在應用程式視窗之間具有獨佔焦點，直到使用者選擇一個選項，而 **HRESULT** 從您對 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 的呼叫傳回程序代碼表示使用者選擇。</span><span class="sxs-lookup"><span data-stu-id="af03d-120">When modal, the dialog box has exclusive focus among application windows until the user chooses an option, and the **HRESULT** return code from your call to [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indicates the user choice.</span></span> <span data-ttu-id="af03d-121">當無模式時，對話方塊不會有獨佔焦點，且您對 **RequestPermissions** 的呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="af03d-121">When modeless, the dialog box does not have exclusive focus and your call to **RequestPermissions** returns immediately.</span></span> <span data-ttu-id="af03d-122">在此情況下，傳回碼會指出方法是否成功，但無法用來確定使用者的選擇。</span><span class="sxs-lookup"><span data-stu-id="af03d-122">In this case, the return code indicates whether the method succeeded, but cannot be used to ascertain the user's choice.</span></span> <span data-ttu-id="af03d-123">接著，您可以藉由處理 [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) 事件並檢查每個感應器的感應器狀態是否就緒，來判斷已啟用的感應器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="af03d-123">You can then determine which sensors have been enabled by handling the [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) event and checking each sensor for SENSOR\_STATE\_READY.</span></span>

<span data-ttu-id="af03d-124">如需傳回碼的詳細資訊，請參閱 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="af03d-124">For more information about return codes, see the [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) reference page.</span></span>

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a><span data-ttu-id="af03d-125">最佳做法：避免對 RequestPermissions 進行多個非模式呼叫</span><span class="sxs-lookup"><span data-stu-id="af03d-125">Best Practice: Avoid Multiple Modeless Calls to RequestPermissions</span></span>

<span data-ttu-id="af03d-126">對 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 的重複非強制回應會顯示多個 [ **啟用這些感應器** ] 對話方塊的實例，而且可能會使用對話方塊來填滿畫面，而導致使用者體驗不佳。</span><span class="sxs-lookup"><span data-stu-id="af03d-126">Repeated modeless calls to [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) will display multiple instances of the **Enable these sensors** dialog box, and can potentially flood the screen with dialog boxes, resulting in a poor user experience.</span></span> <span data-ttu-id="af03d-127">如果您認為第一次呼叫 **RequestPermissions** 之後，可能會安裝其他定位感應器，而需要對 **RequestPermissions** 進行另一次呼叫，您應該以強制回應方式呼叫 **RequestPermissions** ，或等候直到安裝所有定位感應器，以進行非模式呼叫。</span><span class="sxs-lookup"><span data-stu-id="af03d-127">If you think that after your first call to **RequestPermissions**, other location sensors might be installed, requiring another call to **RequestPermissions**, you should either call **RequestPermissions** modally, or wait until all location sensors are installed to make a modeless call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af03d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="af03d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af03d-129">感應器和位置平臺的隱私權與安全性</span><span class="sxs-lookup"><span data-stu-id="af03d-129">Privacy and Security in the Sensor and Location Platform</span></span>](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[<span data-ttu-id="af03d-130">要求使用者權限</span><span class="sxs-lookup"><span data-stu-id="af03d-130">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
