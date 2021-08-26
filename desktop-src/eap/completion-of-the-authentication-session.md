---
title: 完成驗證會話
description: 驗證會話完成之後，驗證服務會呼叫 RasEapEnd 函數，以允許驗證通訊協定解除配置其工作緩衝區。
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee29ac4c4139fc8a575e7570e3c04fbe449aa4d619cea3e096cd12dfcf19bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948468"
---
# <a name="completion-of-the-authentication-session"></a>完成驗證會話

驗證會話完成之後，驗證服務會呼叫 [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) 函數，以允許驗證通訊協定解除配置其工作緩衝區。 無論驗證是否成功，都會執行此動作。 呼叫 **RasEapEnd** 函式可保證不會在第一次呼叫 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))的情況下，使用該特定使用者或內容進行其他的驗證通訊協定呼叫。

 

 