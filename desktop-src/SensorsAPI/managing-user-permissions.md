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
# <a name="managing-user-permissions"></a>管理使用者權限

感應器 API 提供的方法可用來提示使用者使用感應器或感應器集合的許可權。

因為感應器可能會顯示機密資訊，所以 Windows 會要求使用者在您的程式可以存取任何資料之前，先啟用感應器。

當您想要使用目前 [**SENSORSTATE**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) 感應器 \_ 狀態拒絕存取的感應器時，您可能會想要要求許可權 \_ \_ 。

若要要求許可權，請呼叫 [**ISensorManager：： RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 方法。 當您呼叫這個方法時，Windows 會開啟 [ **啟用感應器** ] 對話方塊，提示使用者啟用您所要求的感應器。 此對話方塊會提供使用者您所要求之感應器的名稱。 使用者可以選擇下列其中一個選項：

-   **啟用這些感應器**。
-   **請勿啟用這些感應器**。
-   **開啟主控台以取得更多選項**。

如果使用者選擇 [ **不啟用這些感應器**]，Windows 將不會再顯示那些特定感應器的 [ **啟用感應器** ] 對話方塊，即使您的程式呼叫 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)。 如果使用者選擇任何其他選項，Windows 將允許在要求時顯示對話方塊。 如果您對 **RequestPermissions** 的呼叫包含某些使用者先前選擇要保持停用的感應器，感應器 API 將會從使用者看到的感應器清單中移除這些感應器。

### <a name="modal-or-modeless-behavior"></a>強制回應或非模式行為

[**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)方法會使用 **布林值** 引數，判斷 [**啟用感應器**] 對話方塊是否顯示為強制回應或非強制回應視窗。 這項設定也會影響對話方塊的行為是同步或非同步。

當強制回應時，對話方塊會在應用程式視窗之間具有獨佔焦點，直到使用者選擇一個選項，而 **HRESULT** 從您對 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 的呼叫傳回程序代碼表示使用者選擇。 當無模式時，對話方塊不會有獨佔焦點，且您對 **RequestPermissions** 的呼叫會立即傳回。 在此情況下，傳回碼會指出方法是否成功，但無法用來確定使用者的選擇。 接著，您可以藉由處理 [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) 事件並檢查每個感應器的感應器狀態是否就緒，來判斷已啟用的感應器 \_ \_ 。

如需傳回碼的詳細資訊，請參閱 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 參考頁面。

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>最佳做法：避免對 RequestPermissions 進行多個非模式呼叫

對 [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) 的重複非強制回應會顯示多個 [ **啟用這些感應器** ] 對話方塊的實例，而且可能會使用對話方塊來填滿畫面，而導致使用者體驗不佳。 如果您認為第一次呼叫 **RequestPermissions** 之後，可能會安裝其他定位感應器，而需要對 **RequestPermissions** 進行另一次呼叫，您應該以強制回應方式呼叫 **RequestPermissions** ，或等候直到安裝所有定位感應器，以進行非模式呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[感應器和位置平臺的隱私權與安全性](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[要求使用者權限](requesting-user-permissions.md)
</dt> </dl>

 

 
