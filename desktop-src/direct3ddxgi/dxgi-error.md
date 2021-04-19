---
description: DXGI 函數可傳回的錯誤碼。
ms.assetid: 9aa7dd65-6bf9-4731-8085-a9eab4224cdd
title: 'DXGI_ERROR (Winerror.h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369ab027f41b8b46938bda5d5eba42182a9cbf4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992708"
---
# <a name="dxgi_error"></a>DXGI \_ 錯誤

DXGI 函數可傳回的錯誤碼。



| 常數/值                                                                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ERROR_ACCESS_DENIED"></span><span id="dxgi_error_access_denied"></span><dl> <dt>**DXGI \_\_ \_ 拒絕存取錯誤**</dt> <dt>0x887A002B</dt> </dl>                                                 | 您嘗試使用的資源沒有必要的存取權限。 此錯誤最常見的原因是您寫入具有唯讀存取權的共用資源時。<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DXGI_ERROR_ACCESS_LOST"></span><span id="dxgi_error_access_lost"></span><dl> <dt>**DXGI \_\_存取 \_ 遺失0x887A0026 時發生錯誤**</dt> <dt></dt> </dl>                                                       | 桌面複製介面無效。 當桌面上顯示不同類型的影像時，桌面複製介面通常會變成無效。<br/>                                                                                                                                                                                                                                                                                                                             |
| <span id="DXGI_ERROR_ALREADY_EXISTS"></span><span id="dxgi_error_already_exists"></span><dl> <dt>**DXGI \_錯誤 \_ 已經 \_ 存在**</dt> <dt>0x887A0036L</dt> </dl>                                             | 所需的元素已經存在。 如果不是第一次呼叫函式，則會傳回 [DXGIDeclareAdapterRemovalSupport](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport) 。<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="dxgi_error_cannot_protect_content"></span><dl> <dt>**DXGI \_錯誤 \_ 無法 \_ 保護 \_ 內容**</dt> <dt>0x887A002A</dt> </dl>                     | DXGI 無法在交換鏈上提供內容保護。 此錯誤通常是因為較舊的驅動程式所造成，或您使用與內容保護不相容的交換鏈。<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ERROR_DEVICE_HUNG"></span><span id="dxgi_error_device_hung"></span><dl> <dt>**DXGI \_錯誤 \_ 裝置無 \_ 反應**</dt> <dt>0x887A0006</dt> </dl>                                                       | 應用程式的裝置因應用程式傳送的命令格式錯誤而失敗。 這是設計階段問題，應該加以調查和修正。<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="DXGI_ERROR_DEVICE_REMOVED"></span><span id="dxgi_error_device_removed"></span><dl> <dt>**DXGI \_\_裝置 \_ 已移除的錯誤**</dt> <dt>0x887A0005</dt> </dl>                                              | 視訊卡已實際從系統中移除，或已發生視訊卡的驅動程式升級。 應用程式應該會摧毀並重新建立裝置。 如需協助進行問題的偵錯工具，請呼叫 [**ID3D10Device：： GetDeviceRemovedReason**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-getdeviceremovedreason)。<br/>                                                                                                                                                                                         |
| <span id="DXGI_ERROR_DEVICE_RESET"></span><span id="dxgi_error_device_reset"></span><dl> <dt>**DXGI \_錯誤 \_ 裝置 \_ 重設**</dt> <dt>0x887A0007</dt> </dl>                                                    | 裝置因命令格式錯誤而失敗。 這是執行時間問題;應用程式應該會摧毀並重新建立裝置。<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="dxgi_error_driver_internal_error"></span><dl> <dt>**DXGI \_錯誤 \_ 驅動程式 \_ 內部 \_ 錯誤**</dt> <dt>0x887A0020</dt> </dl>                        | 驅動程式發生問題，並已進入裝置已移除狀態。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="dxgi_error_frame_statistics_disjoint"></span><dl> <dt>**DXGI \_錯誤 \_ 框架 \_ 統計資料 \_ 斷續**</dt> <dt>0x887A000B</dt> </dl>            | 例如，一個事件 (例如，電源週期) 中斷了展示統計資料的收集。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="dxgi_error_graphics_vidpn_source_in_use"></span><dl> <dt>**DXGI \_\_使用0x887A000C 的錯誤圖形 \_ VIDPN \_ 來源 \_ \_**</dt> <dt></dt> </dl> | 應用程式嘗試取得輸出的獨佔擁有權，但失敗，因為應用程式中的某些其他應用程式 (或裝置) 已取得擁有權。<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DXGI_ERROR_INVALID_CALL"></span><span id="dxgi_error_invalid_call"></span><dl> <dt>**DXGI \_錯誤 \_ 不正確 \_ 呼叫**</dt> <dt>0x887A0001</dt> </dl>                                                    | 應用程式提供不正確參數資料;在發行應用程式之前，必須先加以調試和修正。<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DXGI_ERROR_MORE_DATA"></span><span id="dxgi_error_more_data"></span><dl> <dt>**DXGI \_錯誤 \_ 更多 \_ 資料**</dt> <dt>0x887A0003</dt> </dl>                                                             | 應用程式所提供的緩衝區不夠大，無法容納所要求的資料。<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="dxgi_error_name_already_exists"></span><dl> <dt>**DXGI \_錯誤 \_ 名稱 \_ 已 \_ 存在**</dt> <dt>0x887A002C</dt> </dl>                              | 在 [**IDXGIResource1：： CreateSharedHandle**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle) 的呼叫中，提供的資源名稱已經與其他某些資源相關聯。<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="DXGI_ERROR_NONEXCLUSIVE"></span><span id="dxgi_error_nonexclusive"></span><dl> <dt>**DXGI \_錯誤非 \_ 獨佔**</dt> <dt>0x887A0021</dt> </dl>                                                     | 全域計數器資源正在使用中，且 Direct3D 裝置目前無法使用計數器資源。<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="dxgi_error_not_currently_available"></span><dl> <dt>**DXGI \_\_目前無法 \_ \_ 使用的錯誤**</dt> <dt>0x887A0022</dt> </dl>                  | 資源或要求目前無法使用，但稍後可能會變成可用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="DXGI_ERROR_NOT_FOUND"></span><span id="dxgi_error_not_found"></span><dl> <dt>**DXGI \_\_找不 \_ 到錯誤**</dt> <dt>0x887A0002</dt> </dl>                                                             | 呼叫 [**IDXGIObject：： GetPrivateData**](/windows/desktop/api/DXGI/nf-dxgi-idxgiobject-getprivatedata)時，不會將傳入的 GUID 辨識為先前傳遞給 [**IDXGIObject：： SetPrivateData**](/windows/desktop/api/DXGI/nf-dxgi-idxgiobject-setprivatedata) 或 [**IDXGIObject：： SetPrivateDataInterface**](/windows/desktop/api/DXGI/nf-dxgi-idxgiobject-setprivatedatainterface)的 GUID。 呼叫 [**IDXGIFactory：： EnumAdapters**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-enumadapters) 或 [**IDXGIAdapter：： EnumOutputs**](/windows/desktop/api/DXGI/nf-dxgi-idxgiadapter-enumoutputs)時，列舉的序數超出範圍。<br/> |
| <span id="DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="dxgi_error_remote_client_disconnected"></span><dl> <dt>**DXGI \_\_遠端 \_ 用戶端 \_ 中斷連線時發生錯誤**</dt> <dt>0x887A0023</dt> </dl>         | 保留<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="dxgi_error_remote_outofmemory"></span><dl> <dt>**DXGI \_\_遠端 \_ OUTOFMEMORY 錯誤**</dt> <dt>0x887A0024</dt> </dl>                                  | 保留<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="dxgi_error_restrict_to_output_stale"></span><dl> <dt>**DXGI \_錯誤 \_ 限制 \_ 為 \_ 輸出 \_ 過時**</dt> <dt>0x887A0029</dt> </dl>              | DXGI 輸出 (監視已限制交換鏈內容的) ，現在已中斷連線或變更。<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="dxgi_error_sdk_component_missing"></span><dl> <dt>**DXGI \_錯誤 \_ SDK \_ 元件 \_ 遺失**</dt> <dt>0x887A002D</dt> </dl>                        | 作業相依于遺失或不相符的 SDK 元件。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="dxgi_error_session_disconnected"></span><dl> <dt>**DXGI \_錯誤 \_ 會話已 \_ 中斷**</dt>連線 <dt>0x887A0028</dt> </dl>                            | 遠端桌面服務的會話目前已中斷連線。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="DXGI_ERROR_UNSUPPORTED"></span><span id="dxgi_error_unsupported"></span><dl> <dt>**DXGI \_錯誤 \_ 不支援**</dt>的 <dt>0x887A0004</dt> </dl>                                                        | 裝置或驅動程式不支援要求的功能。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DXGI_ERROR_WAIT_TIMEOUT"></span><span id="dxgi_error_wait_timeout"></span><dl> <dt>**DXGI \_錯誤 \_ 等候 \_ 超時**</dt> <dt>0x887A0027</dt> </dl>                                                    | 在下一個桌面畫面格可用之前經過的逾時間隔。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="dxgi_error_was_still_drawing"></span><dl> <dt>**DXGI \_錯誤 \_ \_ 仍在 \_ 繪製**</dt> <dt>0x887A000A</dt> </dl>                                    | 當進行呼叫以執行作業，但未執行或排程作業時，GPU 會處於忙碌狀態。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ 確定**</dt> </dl>                                                                                                                                                                               | 方法成功而沒有錯誤。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>備註

您可能只對方法是否成功或失敗感興趣。 測試 **HRESULT** 值是否會指出成功或失敗的最佳方式，是將值傳遞至下列其中一個在 winerror.h 中定義的宏：

-   [**成功**](/windows/win32/api/winerror/nf-winerror-succeeded)的宏會針對成功代碼傳回 **TRUE** ，並針對失敗碼傳回 **FALSE** 。
-   [**失敗**](/windows/win32/api/winerror/nf-winerror-failed)的宏會針對失敗代碼傳回 **TRUE** ，並針對成功碼傳回 **FALSE** 。

每個 **DXGI \_ 錯誤** 值的 **HRESULT** 值都是由 DXGItype 中定義的這個宏所決定：


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_HRESULT(code) MAKE_HRESULT(1, _FACDXGI, code)
```



例如，在定義為 **0x887A0001** 的情況下， **\_ 發生 DXGI 錯誤 \_ 無效 \_ 呼叫**：


```
#define DXGI_ERROR_INVALID_CALL                 MAKE_DXGI_HRESULT(1)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winerror.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 常數](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
