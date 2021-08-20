---
title: 移植光源和材質函數
description: 適用于光源和材質的 OpenGL 函式與鳶尾花 GL 功能有明顯的差異。 不同于鳶尾花 GL，OpenGL 具有不同的功能，可用於設定燈光、淺色模型和材質。
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- 鳶尾花 GL 移植，光源
- 從鳶尾花 GL、光源移植
- 從鳶尾花 GL （光源）移植至 OpenGL
- 從鳶尾花 GL、光源移植的 OpenGL
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質進行移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL、材質移植的 OpenGL
- 光源
- 材質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45041dde0902f983648c6d258f4c4a8220085d0d8bbeddc6fbdbc970033a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118933028"
---
# <a name="porting-lighting-and-materials-functions"></a>移植光源和材質函數

適用于光源和材質的 OpenGL 函式與鳶尾花 GL 功能有明顯的差異。 不同于鳶尾花 GL，OpenGL 具有不同的功能，可用於設定燈光、淺色模型和材質。

在移植光源和材質功能時，請記住下列幾點：

-   OpenGL 沒有任何已儲存定義的資料表。 您可以使用顯示清單來模仿鳶尾花 GL 定義/系結機制。 如需有關 defs 和系結的詳細資訊，請參閱 [移植 defs、系結和設定](porting-defs--binds--and-sets.md)。
-   使用 OpenGL 時，衰減會與每個光源來源產生關聯，而不是與整體光源模型相關聯。
-   擴散和反射元件會以 OpenGL light 來源分隔。
-   OpenGL light 來源具有 Alpha 元件。 移植您的鳶尾花 GL 程式碼時，請將此 Alpha 元件設為1.0，指出100% 不透明。 Alpha 值接著會由材質的 Alpha 元件決定，因此場景中的物件看起來會像在鳶尾花 GL 中一樣。

下表列出鳶尾花 GL 光源和材質函數及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數                 | OpenGL 函數                               | 意義                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef (DEFLIGHT**，.。。 **)**    | [glLight](gllight-functions.md)              | 定義燈光來源。                                        |
| **Imdef (DEFLMODEL**，.。。 **)**   | [glLightModel](gllightmodel-functions.md)    | 定義光源模型。                                      |
| **Imbind**                       | [**glEnable**](glenable.md) ( GL \_ 燈)  | 啟用 light *i*。                                             |
| **Imbind**                       | **glEnable** ( GL \_ 照明 )                   | 啟用光源。                                              |
| **Imdef (DEFMATERIAL**，.。。 **)** | [**glMaterial**](glmaterial-functions.md)    | 定義材質。                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | 變更使用中的色彩命令效果。 |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | 取得材質參數。                                      |



 

下表列出各種鳶尾花 GL 材質參數及其對等的 OpenGL 參數。



| Imdef 索引  | glMaterial 參數                              | 預設              | 意義                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| 阿 爾 法        | GL \_ 擴散                                       |                      | GL 擴散參數中的第四個值會 \_ 指定 Alpha 值。                      |
| 環境      | GL \_ 環境                                       |  (0.2、0.2、0.2、1.0)  | 環境色彩。                                                                                |
| 彌漫 性      | GL \_ 擴散                                       |  (0.8、0.8、0.8、1.0)  | 擴散色彩。                                                                                |
| 鏡面     | GL \_ 反射                                      |  (0.0、0.0、0.0、1.0)  | 放射色彩。                                                                               |
| 增    | GL \_ SHININESSGL \_ 環境 \_ 和 \_ 擴散<br/> | 0.0                  | 反射指數。相當於呼叫具有相同值的 **glMaterial** 兩次。<br/> |
| COLORINDEXES | GL \_ 色彩 \_ 索引                                |                      | 環境、擴散和反射光源的色彩索引。                                    |



 

當 **Imdef** 的第一個參數為 DEFMODEL 時，對等的 OpenGL 轉譯是函數 [**glLightModel**](gllightmodel-functions.md)。 例外狀況是在 DEFMODEL 後面的參數是衰減時：接著會 [**glLight**](gllight-functions.md)對等的 OpenGL 函數。

下表列出鳶尾花 GL 和 OpenGL 的對等光源模型參數。



| Imdef 索引 | glLightModel 參數          | 預設              | 意義                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| 環境     | GL \_ LIGHT \_ 模型 \_ 環境       |  (0.2、0.2、0.2、1.0)  | 場景的環境色彩。                          |
| 衰減 |                                 |                      | 請參閱 [**glLight**](gllight-functions.md)。        |
| LOCALVIEWER | GL \_ 光 \_ 模型 \_ 本機 \_ 檢視器 | GL \_ FALSE            | 檢視器本機 (**TRUE**) 或無限 (**FALSE**) 。 |
| TWOSIDE     | GL \_ LIGHTMODEL \_ 兩 \_ 端       | GL \_ FALSE            | 當 **為 TRUE** 時，請使用雙面光源。            |



 

當 **Imdef** 的第一個參數為 DEFLIGHT 時，對等的 OpenGL 轉譯為 [**glLight**](gllight-functions.md) 函式。

下表列出鳶尾花 GL 和 OpenGL 的對等光源參數。



| Imdef 索引           | glLight 參數                                                                                 | 預設                                                                             | 意義                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 環境               | GL \_ AMBIENTGL \_ 擴散<br/> GL \_ 反射<br/>                                         |  (0.0、0.0、0.0、1.0)  (1.0、1.0、1.0、1.0) <br/>  (1.0、1.0、1.0、1.0) <br/> | 環境濃度。擴散濃度。<br/> 反射濃度。<br/> |
| LCOLOR                | 沒有同等項目。                                                                                    |                                                                                     |                                                                                |
| POSITION              | GL \_ 位置                                                                                      |  (0.0、0.0、1.0、0.0)                                                                 | 光源的位置。                                                             |
| SPOTDIRECTION         | GL \_ 點 \_ 方向                                                                               |  (0、0、1)                                                                            | 焦點方向。                                                        |
| 聚光燈             | GL \_ 點 \_ EXPONENTGL \_ 點 \_ 截止<br/>                                                     | 0180<br/>                                                                     | 濃度分佈。光線來源的最大散佈角度。<br/>        |
| DEFMODEL、衰減 | GL \_ 常數 \_ ATTENUATIONGL \_ 線性 \_ 衰減<br/> GL \_ 二次 \_ 衰減<br/> |  (1、0、0)                                                                            | 衰減因素。                                                           |



 

 

 





