---
description: 本主題列出適用于脈衝寬度調製的 IOCTLs。
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: PWM 控制項碼
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7de81b26a1970bbecde76729be2f1c84e6c067
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936100"
---
# <a name="pwm-control-codes"></a>PWM 控制項碼

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

本主題列出適用于脈衝寬度調製的 IOCTLs。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                      | 描述                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOCTL \_ PWM \_ 控制器 \_ 取得 \_ 實際 \_ 期間**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | 抓取脈衝寬度調製 (PWM) 控制器的有效輸出信號期間，因為它會在其輸出通道上進行測量。<br/>                                                                                                                                                                                  |
| [**IOCTL \_ PWM \_ 控制器 \_ 取得 \_ 資訊**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | 抓取 (PWM) 控制器的脈衝寬度調製相關資訊。 這項資訊不會在控制器初始化之後變更。 <br/>                                                                                                                                                                                |
| [**IOCTL \_ PWM \_ 控制器 \_ 設定的 \_ 所需 \_ 期限**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | 將脈衝寬度的輸出信號間隔設定 (PWM) 控制器設定為建議的值。 <br/>                                                                                                                                                                                                                            |
| [**IOCTL \_ PWM PIN 取得使用中的工作 \_ \_ \_ \_ \_ 週期 \_ 百分比**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | 抓取釘選或頻道目前的工作週期百分比。 控制項程式碼會以 PWM 的針腳取得使用中的工作 [**\_ \_ \_ \_ \_ 週期 \_ 百分比 \_ 輸出**](pwm-pin-get-active-duty-cycle-percentage-output.md) 結構，傳回百分比。<br/>                                                                                  |
| [**IOCTL \_ PWM \_ 釘選有效的工作 \_ \_ \_ \_ 週期 \_ 百分比**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | 為控制器釘選或通道設定預期的工作週期百分比值。 控制項程式碼會將百分比指定為 PWM 的 PIN 集使用中的工作 [**\_ \_ \_ \_ \_ 週期 \_ 百分比 \_ 輸入**](pwm-pin-set-active-duty-cycle-percentage-input.md) 結構。 <br/>                                                                      |
| [**IOCTL \_ PWM \_ 圖釘 \_ 取得 \_ 極性**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | 抓取 pin 或通道的目前信號極性。 控制項程式碼會以 [**PWM \_ 針腳 \_ 取得 \_ 極性 \_ 輸出**](pwm-pin-get-polarity-output.md) 結構的形式取得信號極性。 信號極性是主動高或主動低，如 [**PWM \_ 極性**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) 列舉中所定義。 <br/> |
| [**IOCTL \_ PWM \_ 固定 \_ 設定 \_ 極性**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | 設定 pin 或通道的信號極性。 控制項程式碼會根據 [**PWM 的 \_ PIN \_ 集 \_ 極性 \_ 輸入**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) 結構來設定信號極性。 信號極性是主動高或主動低，如 [**PWM \_ 極性**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) 列舉中所定義。<br/>           |
| [**IOCTL \_ PWM \_ 釘選 \_ 開始**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | 開始產生脈衝寬度的 (PWM 在 pin 或頻道上) 信號。 若要檢查是否已啟動 pin，請 [**使用 \_ IOCTL \_ PWM \_ 釘 \_**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)選。<br/>                                                                                                                                |
| [**IOCTL \_ PWM \_ 釘選 \_ 停止**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | 停止產生脈衝寬度的 (PWM 在 pin 或頻道上) 信號。 若要檢查是否已啟動 pin，請 [**使用 \_ IOCTL \_ PWM \_ 釘 \_**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)選。<br/>                                                                                                                                 |
| [**已 \_ 啟動 IOCTL PWM \_ 釘選 \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | 抓取 pin 或通道產生信號的狀態。 每個 pin 的狀態都是「已啟動」或「已停止」，因為 [**PWM 的 \_ pin \_ 已 \_ 啟動 \_ 輸出**](pwm-pin-is-started-output.md) 結構。<br/>                                                                                                                                 |



 

 

 




