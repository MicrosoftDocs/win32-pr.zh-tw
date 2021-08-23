---
description: Windows可攜式裝置會定義下列事件值。
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: " (PortableDevice 的事件常數) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5ae8a0a519af32a68bd65241f847cadcaa3d623be932a747e21a3b86338d680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704788"
---
# <a name="event-constants-portabledeviceh"></a> (PortableDevice 的事件常數) 

Windows可攜式裝置會定義下列事件值。



| 常數                                                                                                                                                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**\_已更新 WPD 事件 \_ 裝置 \_ 功能 \_**</dt> </dl> | 此事件表示裝置功能已變更。 如果用戶端根據裝置功能做出任何決策，則應該重新查詢裝置。<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**\_ \_ 已移除 WPD 事件裝置 \_**</dt> </dl>                                         | 當卸載裝置的驅動程式時，就會傳送此事件。 這通常是裝置即將插即用的結果。<br/> 用戶端應該釋放 **IPortableDevice** 介面，以及在 **WPD \_ 事件 \_ 參數 \_ PNP \_ 裝置 \_ 識別碼** 中指定的任何 [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)介面。<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**WPD \_ 事件 \_ 裝置 \_ 重設**</dt> </dl>                                               | 此事件表示裝置即將重設，而且所有連線的用戶端都應該關閉其與裝置的連線。<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**\_ \_ 已新增 WPD 事件物件 \_**</dt> </dl>                                               | 此事件表示裝置上有新的物件可用。<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**WPD \_ 事件 \_ 物件 \_ 已移除**</dt> </dl>                                         | 從裝置移除先前現有的物件之後，就會傳送此事件。<br/> 物件可能是內容物件，例如，已刪除影像檔案。或者，它可能是一個功能物件，例如，新的儲存裝置已從裝置中拔出。<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**已 \_ 要求 WPD 事件 \_ 物件 \_ 傳輸 \_**</dt> </dl>       | 系統會傳送此事件以要求應用程式從裝置傳送特定物件。<br/> 物件通常是內容物件，例如影像檔案。<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**WPD \_ 事件 \_ 物件 \_ 已更新**</dt> </dl>                                         | 此事件是在物件已更新之後傳送，而且任何連線的用戶端都應該重新整理該物件的觀點。<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**WPD \_ 事件 \_ 服務 \_ 方法 \_ 完成**</dt> </dl>             | 當驅動程式已完成叫用服務方法時，就會傳送此事件。 即使方法失敗，也必須傳送此事件。 這是內部 WPD 的 DDI 事件，任何應用程式都不會透過 [**IPortableDevice：： Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) 或 [**IPortableDeviceService：： advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise)提供使用。<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**WPD \_ 事件 \_ 儲存 \_ 格式**</dt> </dl>                                         | 此事件表示儲存物件上的格式作業進度。<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數](constants.md)
</dt> </dl>

 

 




