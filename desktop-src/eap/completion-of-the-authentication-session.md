---
title: 完成驗證會話
description: 驗證會話完成之後，驗證服務會呼叫 RasEapEnd 函數，以允許驗證通訊協定解除配置其工作緩衝區。
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375096"
---
# <a name="completion-of-the-authentication-session"></a>完成驗證會話

驗證會話完成之後，驗證服務會呼叫 [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) 函數，以允許驗證通訊協定解除配置其工作緩衝區。 無論驗證是否成功，都會執行此動作。 呼叫 **RasEapEnd** 函式可保證不會在第一次呼叫 [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))的情況下，使用該特定使用者或內容進行其他的驗證通訊協定呼叫。

 

 