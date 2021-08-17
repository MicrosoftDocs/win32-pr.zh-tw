---
title: " (Direct3D 11) 的資源限制"
description: 本主題包含 Direct3D 11 支援的資源清單 (特別是功能等級11或2.x 硬體) 。
ms.assetid: 80ae49f2-4a6d-4cfc-95d6-510685ab9736
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e54771dafb44164196d44c760c3a60ec96ae2fee138abe7809234b8c4e073c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124136"
---
# <a name="resource-limits-direct3d-11"></a> (Direct3D 11) 的資源限制

本主題包含 Direct3D 11 支援的資源清單 (特別是 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 11 或2.x 硬體) 。

-   [功能等級11硬體的資源限制](#resource-limits-for-feature-level-11-hardware)
-   [功能層級2.x 硬體的資源限制](#resource-limits-for-feature-level-9x-hardware)
-   [相關主題](#related-topics)

## <a name="resource-limits-for-feature-level-11-hardware"></a>功能等級11硬體的資源限制

所有這些資源限制都會定義為 D3d11 中的常數。



| 資源                                                                                               | 限制                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 常數緩衝區中的元素數目                                                                | D3D11 要求的 \_ \_ 常數 \_ 緩衝區 \_ 元素 \_ 計數 (4096)                                                                                                                                                                                                                                                                       |
| 材質 (的數目與緩衝區中的結構大小) 無關                                              | D3D11 \_ 需求 \_ 緩衝區 \_ 資源 \_ 材質 \_ 計數 \_ 2 \_ 到 \_ EXP (2 7) 材質                                                                                                                                                                                                                                                      |
| Texture1D U 維度                                                                                  | D3D11 \_ 需求 \_ TEXTURE1D \_ U \_ 維度 (16384)                                                                                                                                                                                                                                                                               |
| Texture1DArray 維度                                                                               | D3D11 \_ 需求 \_ TEXTURE1D \_ 陣列 \_ 軸 \_ 維度 (2048 陣列配量)                                                                                                                                                                                                                                                         |
| Texture2D U/V 維度                                                                                | D3D11 \_ 需求 \_ TEXTURE2D \_ U \_ 或 \_ V \_ 維度 (16384)                                                                                                                                                                                                                                                                        |
| Texture2DArray 維度                                                                               | D3D11 \_ 需求 \_ TEXTURE2D \_ 陣列 \_ 軸 \_ 維度 (2048 陣列配量)                                                                                                                                                                                                                                                         |
| Texture3D U/V/W 維度                                                                              | D3D11 \_ 需求 \_ TEXTURE3D \_ U \_ V \_ 或 \_ W \_ 維度 (2048)                                                                                                                                                                                                                                                                      |
| TextureCube 維度                                                                                  | D3D11 \_ 需求 \_ TEXTURECUBE \_ 維度 (16384)                                                                                                                                                                                                                                                                                |
| 上述任何資源的資源大小 (MB)                                                | 最小 ( (128，0.25 f \* (專用 VRAM) ) ，2048) MB<br/> D3D11 \_ \_ \_ \_ \_ \_ \_ \_ (128) 的要求資源大小（以 mb 為單位）<br/> D3D11 \_ 要求 \_ 資源 \_ 大小 \_ \_ （以 mb 為單位） \_ \_ \_ (0.25 f) <br/> D3D11 \_ 需求 \_ 資源 \_ 大小 \_ \_ （以 mb 為單位） \_ \_ \_ (2048) <br/> |
| 各向異性篩選 maxanisotropy                                                                    | D3D11 \_ 需求 \_ MAXANISOTROPY (16)                                                                                                                                                                                                                                                                                            |
| 篩選硬體可定址的資源維度                                                   | D3D11 \_ \_ \_ \_ \_ \_ 每個維度 (16384) 的要求篩選 HW 可定址資源維度                                                                                                                                                                                                                                        |
| 資源大小 (MB) 可由 IA (輸入或頂點資料) 或 VS/GS/PS (點範例)               | 最大 (128，0.25 f \* (專用 VRAM) ) MB 的數量<br/> D3D11 \_ \_ \_ \_ \_ \_ \_ \_ (128) 的要求資源大小（以 mb 為單位）<br/> D3D11 \_ 要求 \_ 資源 \_ 大小 \_ \_ （以 mb 為單位） \_ \_ \_ (0.25 f) <br/>                                                                                             |
| 每個內容的資源查看總數 (每個陣列都會計為 1)  (所有檢視類型都有共用限制)  | D3D11 \_ \_ \_ \_ \_ 每個 \_ 裝置 \_ 2 \_ 到 \_ EXP (2 ) 的要求資源查看計數                                                                                                                                                                                                                                                         |
| 多元素) 的緩衝區結構大小 (                                                                  | D3D11 \_ 要求 \_ \_ 的多重 \_ 元素 \_ 結構 \_ 大小 \_ （以位元組為單位） (2048 個位元組)                                                                                                                                                                                                                                                       |
| 資料流程輸出大小                                                                                     | 與緩衝區中的材質數目相同 (請參閱前面的)                                                                                                                                                                                                                                                                  |
| 繪製或 DrawInstanced 頂點計數 (包含實例)                                               | D3D11 \_ 需求 \_ 繪製 \_ 頂點 \_ 計數 \_ 2 \_ 到 \_ EXP (2 )                                                                                                                                                                                                                                                                         |
| DrawIndexed \[ 實例 \] () 頂點計數 (包括實例)                                          | D3D11 \_ 需求 \_ DRAWINDEXED \_ 索引 \_ 計數 \_ 2 \_ 到 \_ EXP (2 )                                                                                                                                                                                                                                                                   |
| GS 調用輸出資料 (元件 \* 頂點)                                                      | D3D11 \_ \_ 實例之間的最大 GS \_ 輸出 \_ 頂點 \_ 計數 \_ \_ (1024)                                                                                                                                                                                                                                                           |
| 每個內容的取樣器物件總數                                                            | D3D11 \_ \_ 每個裝置的要求取樣器 \_ 物件 \_ 計數 \_ \_ (4096)                                                                                                                                                                                                                                                                    |
| 每個管線的各區/剪物件總數                                                  | \_ \_ 每個管線的 D3D11 視口和 \_ SCISSORRECT \_ 物件 \_ 計數 \_ \_ (16)                                                                                                                                                                                                                                                      |
| 每個頂點的剪輯/挑選距離總數                                                         | D3D11 \_ 剪輯 \_ 或 \_ 挑選 \_ 距離 \_ 計數 (8)                                                                                                                                                                                                                                                                                |
| 每個內容的 blend 物件總數                                                              | D3D11 \_ \_ \_ \_ 每個裝置的 (需求 BLEND 物件計數 \_ \_ 4096)                                                                                                                                                                                                                                                                      |
| 每個內容的深度/樣板物件總數                                                      | D3D11 \_ \_ 每個裝置的要求深度樣板 \_ \_ 物件 \_ 計數 \_ \_ (4096)                                                                                                                                                                                                                                                             |
| 每個內容的轉譯器狀態物件總數                                                   | D3D11 \_ 每個裝置的要求轉譯器 \_ \_ 物件 \_ 計數 \_ \_ (4096)                                                                                                                                                                                                                                                                 |
| 取樣時的每個圖元最大取樣計數                                                    | D3D11 \_ 最大多 \_ \_ 取樣取樣 \_ 計數 (32)                                                                                                                                                                                                                                                                               |
| 著色器資源頂點-元素計數 (4 32 位元件)                                           | D3D11 \_ 標準 \_ 頂點 \_ 元素 \_ 計數 (32)                                                                                                                                                                                                                                                                              |
| 常見的著色器核心 (4 32 位元件) temp-註冊計數 (r \# + 可編制索引的 x \# \[ n \])              | D3D11 \_ COMMONSHADER \_ TEMP \_ REGISTER \_ COUNT (4096)                                                                                                                                                                                                                                                                         |
| 一般著色器核心常數緩衝區位置                                                               | D3D11 \_ COMMONSHADER \_ 常數 \_ 緩衝區 \_ HW \_ 插槽 \_ 計數 (15)  (+ 1，在著色器中為立即常數緩衝區設定)                                                                                                                                                                                                    |
| 一般著色器核心輸入-資源插槽                                                                | D3D11 \_ COMMONSHADER \_ 輸入 \_ 資源 \_ 註冊 \_ 計數 (128)                                                                                                                                                                                                                                                               |
| 一般著色器核心取樣器位置                                                                       | D3D11 \_ COMMONSHADER \_ 取樣器 \_ 插槽 \_ 計數 (16)                                                                                                                                                                                                                                                                            |
| 一般著色器核心副程式-嵌套限制                                                            | D3D11 \_ COMMONSHADER \_ 副程式 \_ 嵌套 \_ 限制 (32)                                                                                                                                                                                                                                                                      |
| 一般著色器核心流程式控制制的嵌套限制                                                          | D3D11 \_ COMMONSHADER \_ FLOWCONTROL \_ \_ (64) 的嵌套限制                                                                                                                                                                                                                                                                    |
| 頂點著色器輸入-註冊計數 (4 32 位元件)                                             | D3D11 \_ 和 \_ 輸入暫存器 \_ \_ 計數 (32)                                                                                                                                                                                                                                                                                    |
| 頂點著色器輸出-註冊計數 (4 32 位元件)                                            | D3D11 \_ VS \_ OUTPUT \_ REGISTER \_ COUNT (32)                                                                                                                                                                                                                                                                                   |
| 幾何著色器輸入-註冊計數 (4 32 位元件)                                           | D3D11 \_ GS \_ 輸入 \_ REGISTER \_ COUNT (32)                                                                                                                                                                                                                                                                                    |
| 幾何著色器輸出-註冊計數 (4 32 位元件)                                          | D3D11 \_ GS \_ 輸出暫存器 \_ \_ 計數 (32)                                                                                                                                                                                                                                                                                   |
| 圖元著色器輸入-)  (4 32 位元件的暫存器計數                                             | D3D11 \_ PS \_ 輸入 \_ REGISTER \_ COUNT (32)                                                                                                                                                                                                                                                                                    |
| 圖元著色器輸出位置                                                                              | 8                                                                                                                                                                                                                                                                                                                        |
| 圖元著色器輸出深度暫存器計數 (1 32 位元件)                                          | D3D11 \_ PS \_ 輸出 \_ 深度 \_ 註冊 \_ 計數 (1)                                                                                                                                                                                                                                                                             |
| 輸入組合語言索引輸入資源插槽                                                             | D3D11 \_ IA \_ 索引 \_ 輸入 \_ 資源 \_ 插槽 \_ 計數 (1)                                                                                                                                                                                                                                                                        |
| 輸入組合語言頂點輸入資源插槽                                                            | D3D11 \_ IA \_ 頂點 \_ 輸入 \_ 資源 \_ 位置 \_ 計數 (32)                                                                                                                                                                                                                                                                      |
| 輪廓著色器控制點輸入-註冊計數 (4 32 位元件)                                 | D3D11 \_ HS \_ 控制點 \_ \_ 階段輸入暫存器 \_ \_ \_ 計數 (32)                                                                                                                                                                                                                                                             |
| 輸入控制點的輪廓著色器數目                                                             | D3D11 \_ HS \_ 控制點 \_ \_ REGISTER \_ 元件 \_ 位 \_ 計數 (32)                                                                                                                                                                                                                                                           |
| 輪廓著色器控制項點輸出-註冊計數 (4 32 位元件)                                | D3D11 \_ HS \_ 控制點 \_ \_ 階段 \_ 輸出 \_ 註冊 \_ 計數 (32)                                                                                                                                                                                                                                                            |
| 輸出控制點的輪廓著色器數目                                                            | D3D11 \_ HS \_ 控制點 \_ \_ REGISTER \_ 元件 \_ 位 \_ 計數 (32)                                                                                                                                                                                                                                                           |
| 輪廓著色器修補程式常數輸出- (4 32 位元件的暫存器計數)                               | D3D11 \_ HS \_ 輸出 \_ PATCH \_ \_ \_ (32) 的固定登錄計數                                                                                                                                                                                                                                                                 |
| 網域著色器控制點輸入-註冊計數 (4 32 位元件)                               | D3D11 \_ DS \_ 輸入 \_ 控制 \_ 點 \_ 登錄 \_ 計數 (32)                                                                                                                                                                                                                                                                    |
| 輸入控制點的網域著色器數目                                                           | D3D11 \_ DS \_ 輸入 \_ 控制 \_ 點 \_ 登錄 \_ 元件 \_ 位 \_ 計數 (32)                                                                                                                                                                                                                                                    |
| 網域著色器修補固定輸入-註冊計數 (4 32 位元件)                              | D3D11 \_ DS \_ 輸入 \_ 修補程式 \_ 常數登錄 \_ \_ 計數 (32)                                                                                                                                                                                                                                                                   |
| 網域著色器鑲嵌頂點輸出-)  (4 32 位元件的暫存器計數                        | D3D11 \_ DS \_ OUTPUT \_ REGISTER \_ COUNT (32)                                                                                                                                                                                                                                                                                   |
| 計算著色器未排序存取視圖 (UAV) 位置                                                       | D3D11 \_ PS \_ CS \_ UAV \_ REGISTER \_ COUNT (8) 4                                                                                                                                                                                                                                                                                 |
| 資源磚大小（位元組）                                                                            | D3D11 \_ 2 \_ \_ \_ \_ \_ 以位元組為單位分割資源磚大小 \_ ( 65536 )                                                                                                                                                                                                                                                                |



 

 應用程式可以嘗試配置比資源大小上限指定的資源更多的記憶體。 也就是說，當硬體可能支援這些記憶體配置時，Direct3D 11 執行時間會允許這些嘗試。 不過，Direct3D 11 執行時間只會保證所有 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 11 硬體都支援資源大小上限內的配置。 如果應用程式嘗試在資源大小上限內配置資源的記憶體，則只有在作業系統用盡資源時，執行時間才會失敗。 如果應用程式嘗試配置超過資源大小上限的資源記憶體，執行時間可能會因為作業系統 overextended 或硬體不支援超過資源大小上限的配置而失敗。 Debug 層只會檢查 D3D11 \_ 需求 \_ 資源 \_ 大小 \_ \_ （以 mb 為單位） \_ \_ ， \_ (128) MB。

 圖元著色器輸出位置會在圖元輸出暫存器 (4 32 位元件) 和 UAVs 之間共用。

 所有輪廓著色器指向網域著色器控制點的元件總數限制為3968，128小於控制點最大控制點乘以四個元件的最大控制點數目。

4For 計算著色器設定檔 CS \_ 4 \_ 0 和 cs \_ 4 \_ 1 只有1個可用的 UAV。 如需著色器設定檔的詳細資訊，請參閱 [著色器模型 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)。

## <a name="resource-limits-for-feature-level-9x-hardware"></a>功能層級2.x 硬體的資源限制

所有的 2.x [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 資源限制都會定義為 D3dcommon 中的常數。



| 資源                                                                                                                                            | 限制                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 texture1D U 維度                       | D3D \_ FL9 \_ 1 \_ 要求 \_ TEXTURE1D \_ U \_ 維度 (2048)           |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 3 texture1D U 維度                       | D3D \_ FL9 \_ 3 \_ 要求 \_ TEXTURE1D \_ U \_ 維度 (4096)           |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 Texture2D U/V 維度                     | D3D \_ FL9 \_ 1 \_ 要求 \_ TEXTURE2D \_ U \_ 或 \_ V \_ 維度 (2048)    |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 3 Texture2D U/V 維度                     | D3D \_ FL9 \_ 3 \_ 要求 \_ TEXTURE2D \_ U \_ 或 \_ V \_ 維度 (4096)    |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 Texture3D U/V/W 維度                   | D3D \_ FL9 \_ 1 \_ 需求 \_ TEXTURE3D \_ U \_ V \_ 或 \_ W \_ 維度 (256)  |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 textureCube 維度                       | D3D \_ FL9 \_ 1 \_ 要求 \_ TEXTURECUBE \_ 維度 (512)             |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 3 textureCube 維度                       | D3D \_ FL9 \_ 3 \_ 需求 \_ TEXTURECUBE \_ 維度 (4096)            |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 maxanisotropy 預設值 | D3D \_ FL9 \_ 1 \_ DEFAULT \_ MAX \_ ANISOTROPY (2)                  |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 最大輸入組合語言          | D3D \_ FL9 \_ 1 \_ IA \_ 基本 \_ 最大 \_ 計數 (65535)             |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 2 最大輸入組合器基本          | D3D \_ FL9 \_ 2 \_ IA \_ 基本 \_ 最大 \_ 計數 (1048575)           |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 同時呈現目標                 | D3D \_ FL9 \_ 1 \_ 同時 \_ 呈現 \_ 目標 \_ 計數 (1)       |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 3 同時呈現目標                 | D3D \_ FL9 \_ 3 \_ 同時 \_ 呈現 \_ 目標 \_ 計數 (4)       |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 1 最大材質重複                      | D3D \_ FL9 \_ 1 \_ 最大 \_ 材質 \_ 重複 (128)                    |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 2 最大材質重複                      | D3D \_ FL9 \_ 2 \_ 最大 \_ 材質 \_ 重複 (2048)                   |
| [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ 3 最大材質重複                      | D3D \_ FL9 \_ 3 \_ 最大 \_ 材質 \_ 重複 (8192)                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源](overviews-direct3d-11-resources.md)
</dt> </dl>

 

