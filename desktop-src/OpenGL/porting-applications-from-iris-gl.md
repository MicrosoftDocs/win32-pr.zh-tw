---
title: 從鳶尾花 GL 移植應用程式
description: 從鳶尾花 GL 移植應用程式
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- Windows 上的 OpenGL，鳶尾花 GL 移植
- 移植至 OpenGL、鳶尾花 GL
- OpenGL 移植，鳶尾花 GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68e218e5b6f57039e364ab4e6ebc29fb1f2b2fad2e8a679b35c1368367f5f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777228"
---
# <a name="porting-applications-from-iris-gl"></a>從鳶尾花 GL 移植應用程式

本節列出鳶尾花 GL 和 OpenGL 之間的重要差異，並說明將程式碼從鳶尾花 GL 移植至 OpenGL 的基本步驟。 如需鳶尾花 GL 和 Open GL 之間差異的完整清單，請參閱 [鳶尾花 gl 和 OpenGL 差異](iris-gl-and-opengl-differences.md)。

將鳶尾花 GL 程式移植至 opengl for Windows 需要比從 X 視窗系統轉換 opengl 程式更多的工作。 雖然鳶尾花 GL 程式是設計來搭配特定的硬體和軟體來執行，但 OpenGL 是針對各種系統之間的可攜性而設計的。

下表列出 OpenGL 與鳶尾花 GL 程式之間的一些主要差異。



| OpenGL 程式碼                                                                                                                                              | 鳶尾花 GL 程式碼                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 獨立作業系統;未包含視窗化、事件處理、緩衝區配置/管理等功能。                              | 相依于作業系統;視窗化系統函數會與轉譯函數混合使用。 鳶尾花 GL 中沒有任何 windows 管理員。 |
| 使用標準的通用命名慣例。 OpenGL 函數和定義型別開頭為 "gl" 前置詞，以防止與其他程式庫發生衝突。        | 不使用函數和定義型別的一般命名慣例。                                                              |
| 直接且一致地管理狀態變數 (例如色彩、霧化、材質、光源等) 。 不使用資料表來載入狀態變數值。 | 使用資料表管理狀態變數，且必須將變數系結至資料表值。                                                        |
| 無法編輯顯示清單。                                                                                                                          | 可以編輯顯示清單。                                                                                                          |
| 未提供字型的檔案格式。                                                                                                                | 提供函式來處理字型和文字字串以及字型的檔案格式。                                                      |
| 包含 GL 公用程式 (X.GLU 隊) 程式庫，其中包含額外的函式和常式 (例如 NURBS 和二次轉譯常式) 。                    | 不支援 X.GLU 隊程式庫。                                                                                                     |



 

**使用下列一般程式，將您的鳶尾花 GL 程式移植至 OpenGL**

1.  重寫任何呼叫視窗管理員、視窗設定、裝置或事件的程式碼，或是您將色彩對應載入至相等 Windows 程式碼的程式碼。 將應用程式從一個作業系統重寫為另一個作業系統可能很複雜而且很困難。 本主題已超出本節的範圍。
2.  找出使用鳶尾花 GL 函數和常式的任何程式碼。 將這些函式轉譯為其對等的 OpenGL 函數。 如需鳶尾花 GL 函式和常式及其對等的 OpenGL 對應專案的完整清單，請參閱 OpenGL 函式 [及其鳶尾花 GL](opengl-functions-and-their-iris-gl-equivalents.md)對應專案。
3.  變更鳶尾花 GL 程式碼，如 [特殊鳶尾花 Gl 移植問題](special-iris-gl-porting-issues.md)中所述。

<!-- -->

1.  重寫任何呼叫視窗管理員、視窗設定、裝置或事件的程式碼，或是您將色彩對應載入至相等 Windows 程式碼的程式碼。 將應用程式從一個作業系統重寫為另一個作業系統可能很複雜而且很困難。 本主題已超出本節的範圍。
2.  找出使用鳶尾花 GL 函數和常式的任何程式碼。 將這些函式轉譯為其對等的 OpenGL 函數。 如需鳶尾花 GL 函式和常式及其對等的 OpenGL 對應專案的完整清單，請參閱 OpenGL 函式 [及其鳶尾花 GL](opengl-functions-and-their-iris-gl-equivalents.md)對應專案。
3.  變更鳶尾花 GL 程式碼，如 [特殊鳶尾花 Gl 移植問題](special-iris-gl-porting-issues.md)中所述。

 

 




