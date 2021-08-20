---
title: 移植意見函數
description: 使用鳶尾花 GL，處理意見反應的方式會因執行鳶尾花 GL 的電腦而有所不同。
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- 鳶尾花 GL 移植，意見反應
- 從鳶尾花 GL 進行移植，意見反應
- 從鳶尾花 GL 移植至 OpenGL，意見反應
- 鳶尾花 GL 的 OpenGL 移植，意見反應
- 意見回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f4ab584dfbd9038d45e7d24c006857f278a9239fc6f9da4d38a75363f0d585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132630"
---
# <a name="porting-feedback-functions"></a>移植意見函數

使用鳶尾花 GL，處理意見反應的方式會因執行鳶尾花 GL 的電腦而有所不同。 OpenGL 可將意見反應函式標準化，讓您可以依賴各種硬體平臺之間的一致意見反應。 下表列出鳶尾花 GL 意見反應函式及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數 | OpenGL 函數                                                                                            | 意義                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **回饋**     | [**glRenderMode**](glrendermode.md) ( GL \_ 意見反應 )                                                       | 切換至意見反應模式。                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) ( GL 轉譯 \_ ) [ **glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | 切換至轉譯模式。                   |
| **通過**  | [**glPassThrough**](glpassthrough.md)                                                                     | 將權杖標記放在意見緩衝區中。 |



 

 

 





