---
title: 安全性應用程式偵測規則更新
description: 安全性應用程式偵測規則更新
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024225"
---
# <a name="security-app-detection-rules-update"></a>安全性應用程式偵測規則更新

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


### <a name="description"></a>Description

在 Windows 8 中新增的 Windows Store 應用程式全部都安裝到 [Program Files] 下的一般位置， (% programfiles% ) 稱為 [ \\ program files \\ WindowsApps]。

### <a name="manifestation"></a>表現

這可能會使現有的設定發生衝突，而某些防毒軟體/反惡意程式碼偵測器會將這個位置視為原因的可能位置。

### <a name="mitigation"></a>降低

目前的建議如下：

-   移離 [ \\ 程式檔] \\ WindowsApps 以儲存任何自訂應用程式
-   防毒軟體廠商應該更新其啟發學習法，使其不會將該位置識別為惡意程式碼位置

 

 




