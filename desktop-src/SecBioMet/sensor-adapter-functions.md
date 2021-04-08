---
title: 感應器介面卡功能
description: 感應器介面卡會包裝生物特徵辨識裝置，並提供標準介面，讓 Windows 生物特徵辨識服務設定感應器、捕捉範例，以及控制生物特徵辨識資料流程向處理引擎的流程。
ms.assetid: 32cf28d3-cb78-442d-81db-7827f55b0ba8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cefc5e9221a56a7766e6af6a47449db4405b369
ms.sourcegitcommit: 8a30948ba97ab969fcaa7f7ff05b853f59d8bd5c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/14/2020
ms.locfileid: "103681614"
---
# <a name="sensor-adapter-functions"></a>感應器介面卡功能

感應器介面卡會包裝生物特徵辨識裝置，並提供標準介面，讓 Windows 生物特徵辨識服務設定感應器、捕捉範例，以及控制生物特徵辨識資料流程向處理引擎的流程。 下列函式必須由介面卡的開發人員執行。 Windows 生物識別服務會呼叫它們。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                           | 描述                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/>     | 將校正資料從引擎介面卡傳遞給感應器介面卡。<br/>                                                                                            |
| [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/>                               | 讓感應器介面卡有機會執行任何需要的工作，讓感應器元件退出閒置狀態。<br/>                                                |
| [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                   | 將感應器介面卡新增至生物特徵辨識設備的處理管線。<br/>                                                                                           |
| [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                   | 取消所有擱置中的感應器作業。<br/>                                                                                                                            |
| [**SensorAdapterClearCoNtext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                       | 準備新作業的生物特徵辨識單位處理管線。<br/>                                                                                       |
| [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                         | 執行不需要較高許可權的廠商定義控制項作業。<br/>                                                                             |
| [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>     | 執行需要更高許可權的廠商定義控制項作業。<br/>                                                                                     |
| [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/>                           | 讓感應器介面卡有機會執行將感應器元件進入閒置狀態所需的任何工作。<br/>                                                    |
| [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                   | 釋放附加至管線的介面卡特定資源。<br/>                                                                                                     |
| [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>               | 抓取格式化為標準 [**WINBIO \_ BIR**](winbio-bir.md) 結構的最新已捕獲生物特徵辨識範例。<br/>                                        |
| [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                     | 由 Windows 生物特徵辨識架構呼叫以等候 SensorAdapterStartCapture 函式所起始的捕獲作業完成。<br/>                                                                                       |
| [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)<br/>           | 抓取值，指出感應器指標是開啟或關閉。<br/>                                                                                       |
| [*SensorAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/>               | 接收有關電腦電源狀態變更的通知，並據以準備感應器介面卡。<br/>                                                     |
| [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/>                 | 讓感應器介面卡有機會執行任何清除，這需要引擎或存放裝置介面卡元件的協助。<br/>                                   |
| [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/>                       | 讓感應器介面卡有機會執行任何不完整的初始化，而這需要引擎或存放裝置介面卡元件的協助。<br/> |
| [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>               | 使範例緩衝區的目前內容可供引擎介面卡使用。<br/>                                                                                  |
| [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> | 決定感應器介面卡所支援的一組校正格式。<br/>                                                                                        |
| [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/>             | 決定生物特徵辨識感應器元件的功能和限制。<br/>                                                                                    |
| [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                         | 捕獲感應器裝置目前狀態的相關資訊。<br/>                                                                                              |
| [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                     | 重新初始化感應器。<br/>                                                                                                                                         |
| [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/>       | 通知感應器介面卡，引擎介面卡已選取特定的校正資料格式。<br/>                                                    |
| [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)<br/>           | 開啟或關閉感應器指示燈。<br/>                                                                                                                           |
| [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                 | 設定感應器介面卡模式。<br/>                                                                                                                                     |
| [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                       | 開始非同步生物特徵辨識捕捉。<br/>                                                                                                                         |
| [**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)<br/>                         | 抓取感應器介面卡的 [**WINBIO \_ 感應器 \_ 介面**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface) 結構指標。<br/>                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[外掛程式函數](plug-in-functions.md)
</dt> </dl>

 

 





