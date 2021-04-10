---
title: 感應器介面卡包裝函式
description: 您可以用來在感應器介面卡上呼叫函式的函式。 這些函式定義于 Winbio \_ adapter. h 中。
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8887da38a7142c830f19a83b5950abea15791b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092289"
---
# <a name="sensor-adapter-wrappers"></a>感應器介面卡包裝函式

下列包裝函式是在 Winbio \_ adapter. h 中定義。 您可以使用它們來呼叫感應器介面卡上的函式。



| 函式                                     | 描述                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioSensorAcceptCalibrationData<br/>   | 呼叫 [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>     |
| WbioSensorActivate<br/>                | 呼叫 [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                               |
| WbioSensorAttach<br/>                  | 呼叫 [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn) 函數。<br/>                                                                                                         |
| WbioSensorCancel<br/>                  | 呼叫 [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn) 函數。<br/>                                                                                                         |
| WbioSensorClearCoNtext<br/>            | 呼叫 [**SensorAdapterClearCoNtext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn) 函數。<br/>                                                                                             |
| WbioSensorControlUnit<br/>             | 呼叫 [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn) 函數。<br/>                                                                                               |
| WbioSensorControlUnitPrivileged<br/>   | 呼叫 [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn) 函數。<br/>                                                                           |
| WbioSensorDeactivate<br/>              | 呼叫 [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                           |
| WbioSensorDetach<br/>                  | 呼叫 [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn) 函數。<br/>                                                                                                         |
| WbioSensorExportSensorData<br/>        | 呼叫 [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn) 函數。<br/>                                                                                     |
| WbioSensorFinishCapture<br/>           | 呼叫 [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn) 函數。<br/>                                                                                           |
| WbioSensorNotifyPowerChange<br/>       | 呼叫 [**SensorAdapterNotifyPowerChange**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn) 函數。<br/> 從 Windows 8 開始，支援這個包裝函式函數。<br/>              |
| WbioSensorPipelineCleanup<br/>         | 呼叫 [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                 |
| WbioSensorPipelineInit<br/>            | 呼叫 [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                       |
| WbioSensorPushDataToEngine<br/>        | 呼叫 [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn) 函數。<br/>                                                                                     |
| WbioSensorQueryCalibrationFormats<br/> | 呼叫 [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/> |
| WbioSensorQueryExtendedInfo<br/>       | 呼叫 [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>             |
| WbioSensorQueryStatus<br/>             | 呼叫 [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn) 函數。<br/>                                                                                               |
| WbioSensorReset<br/>                   | 呼叫 [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn) 函數。<br/>                                                                                                           |
| WbioSensorSetCalibrationFormat<br/>    | 呼叫 [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>       |
| WbioSensorSetMode<br/>                 | 呼叫 [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) 函數。<br/>                                                                                                       |
| WbioSensorStartCapture<br/>            | 呼叫 [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn) 函數。<br/>                                                                                             |



 

[**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)和 [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)函數沒有包裝函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[感應器介面卡功能](sensor-adapter-functions.md)
</dt> <dt>

[外掛程式函數](plug-in-functions.md)
</dt> </dl>

 

 





