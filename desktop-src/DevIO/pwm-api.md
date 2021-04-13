---
description: 脈衝寬度調整 (PWM) 是產生矩形脈衝波的技術，其會經過調製的脈衝寬度，以產生波形的平均值變化。
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510572"
---
# <a name="pwm-api"></a>PWM API

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

脈衝寬度調整 (PWM) 是產生矩形脈衝波的技術，其會經過調製的脈衝寬度，以產生波形的平均值變化。 最常見的用法包括驅動的是最高的，也就是降低 Led 或其他相關功能。 PWM 主要用於物聯網案例。

## <a name="about-pulse-width-modulation"></a>關於脈衝寬度調製

PWM 波形可以依兩個參數分類：

-   波形句號 (T) 

-   工作週期，其中波形頻率 (f) 是句號 f = 1/T 之間的倒數

工作週期描述的是使用 **中** 時間的比例（ / 相對於定期間隔或 **期間**）。 較低的工作週期會對應到平均低輸出電源，因為大部分的時間都有電源關閉。 工作週期以百分比表示。 完全開啟于100%。 完全關閉是0%。 使用 **中一半的** 時間是50%。

想要在 IoT 應用程式中執行 PWM 的開發人員，應該調查 [WINRT PWM 檔。](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>脈衝寬度的調製類型

PWM 會使用 [這些 IO 控制碼](pwm-control-codes.md)、 [結構](pwm-structures.md)和列舉 [。](pwm-enumeration-types.md)

PWM 也會使用下列函數： [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath)。

 

 
