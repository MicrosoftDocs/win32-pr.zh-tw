---
description: 此區段會指定 Direct3D Feature 10Level9 9.3 硬體支援的格式 ([ **DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Direct3D 功能 10Level9 9.3 硬體的格式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ad2746ce0d6e277f04783ae7140f3855fa7078e9a50b67d1e52bc827403c4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951276"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a>Direct3D 功能 10Level9 9.3 硬體的格式支援

此區段會指定 Direct3D Feature 10Level9 9.3 硬體支援的格式 ([ **DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。

下表摘要說明使用下列索引鍵的功能支援。

| 符號                            | 描述                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | 不允許或無法使用。                                                  |
| ![必要](images/letter-r.jpg)  | 需要硬體支援。                                                 |
| ![選用](images/letter-o.jpg)  | 硬體支援是選擇性的，格式可能或可能不會有硬體加速。 |
| ![依賴](images/letter-d.jpg) | 如果支援相關的選擇性功能，則為必要項。                            |

本主題包含每一種格式的區段。 格式 *目標* (資料表每個目標各包含一個資料列) 可以是資源類型、HLSL 內建函式，或是相依于特定格式的特定功能。

若要以程式設計方式驗證 D3D11 和 D3D12 中的格式支援，請參閱 [檢查硬體功能支援](checking-hardware-feature-support.md)。

> [!NOTE] 
> 這些格式的數目大多是（但不是全部），以遞增的數值順序來 &mdash; 看，有些會超出數值順序，並與其他相關的格式一起列出。 另請注意 *，格式名稱的無* 型別可以表示 *部分* 具型別，而不是嚴格的無型別 (請參閱主題結尾的 [格式附注](#format-notes) 章節) 。

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 0 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 無的 \_ <sup>電腦</sup> (1) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 128 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ FLOAT<sup>FNS</sup> (2) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 128 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FNS</sup> (3) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 128 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ 聖<sup>FNS</sup> (4) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 128 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 無的 \_ <sup>電腦</sup> (5) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 96 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a>DXGI_FORMAT_R32G32B32 \_ FLOAT<sup>FNS</sup> (6) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 96 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | ![依賴](images/letter-d.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | ![依賴](images/letter-d.jpg) |
| 8x 多重採樣 RenderTarget | ![依賴](images/letter-d.jpg) |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a>DXGI_FORMAT_R32G32B32 \_ UINT<sup>FNS</sup> (7) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 96 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | ![依賴](images/letter-d.jpg) |
| 8x 多重採樣 RenderTarget | ![依賴](images/letter-d.jpg) |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a>DXGI_FORMAT_R32G32B32 \_ 聖<sup>FNS</sup> (8) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 96 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | ![依賴](images/letter-d.jpg) |
| 8x 多重採樣 RenderTarget | ![依賴](images/letter-d.jpg) |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 無別 \_ <sup>電腦</sup> (9) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ FLOAT<sup>FNS</sup> (10) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![選用](images/letter-o.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ UINT<sup>FNS</sup> (12) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ 聖<sup>FNS</sup> (14) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 無別 \_ <sup>電腦</sup> (15) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a>DXGI_FORMAT_R32G32 \_ FLOAT<sup>FNS</sup> (16) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a>DXGI_FORMAT_R32G32 \_ UINT<sup>FNS</sup> (17) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a>DXGI_FORMAT_R32G32 \_ 聖<sup>FNS</sup> (18) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 無別 \_ <sup>電腦</sup> (19) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a>DXGI_FORMAT_D32 \_ FLOAT \_ S8X24 \_ UINT<sup>FNS</sup> (20) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a>DXGI_FORMAT_R32 \_ FLOAT X8X24 無型別 \_ \_ <sup>FNS</sup> (21) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a>DXGI_FORMAT_X32 無別 \_ \_ G8X24 \_ UINT<sup>FNS</sup> (22) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 無別 \_ <sup>電腦</sup> (23) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FNS</sup> (25) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM<sup>FNS</sup> (89) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ FLOAT<sup>FNS</sup> (26) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 無別 \_ <sup>電腦</sup> (27) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | ![必要](images/letter-r.jpg) |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![必要](images/letter-r.jpg) |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (29) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | ![必要](images/letter-r.jpg) |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![必要](images/letter-r.jpg) |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ UINT<sup>FNS</sup> (30) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ 聖<sup>FNS</sup> (32) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 無的 \_ <sup>電腦</sup> (33) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a>DXGI_FORMAT_R16G16 \_ FLOAT<sup>FNS</sup> (34) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a>DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a>DXGI_FORMAT_R16G16 \_ UINT<sup>FNS</sup> (36) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a>DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a>DXGI_FORMAT_R16G16 \_ 聖<sup>FNS</sup> (38) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 無的 \_ <sup>電腦</sup> (39) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a>DXGI_FORMAT_D32 \_ FLOAT<sup>FNS</sup> (40) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a>DXGI_FORMAT_R32 \_ FLOAT<sup>FNS</sup> (41) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | ![必要](images/letter-r.jpg) |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a>DXGI_FORMAT_R32 \_ UINT<sup>FNS</sup> (42) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | ![必要](images/letter-r.jpg) |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a>DXGI_FORMAT_R32 \_ 聖<sup>FNS</sup> (43) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 無的 \_ <sup>電腦</sup> (44) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | ![必要](images/letter-r.jpg) |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a>DXGI_FORMAT_R24 \_ UNORM \_ X8 無別 \_ <sup>FNS</sup> (46) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a>DXGI_FORMAT_X24 無別 \_ \_ G8 \_ UINT<sup>FNS</sup> (47) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 無的 \_ <sup>電腦</sup> (48) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a>DXGI_FORMAT_R8G8 \_ UINT<sup>FNS</sup> (50) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a>DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a>DXGI_FORMAT_R8G8 \_ 聖<sup>FNS</sup> (52) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 無的 \_ <sup>電腦</sup> (53) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a>DXGI_FORMAT_R16 \_ FLOAT<sup>FNS</sup> (54) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a>DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | ![必要](images/letter-r.jpg) |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a>DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a>DXGI_FORMAT_R16 \_ UINT<sup>FNS</sup> (57) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | ![必要](images/letter-r.jpg) |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a>DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a>DXGI_FORMAT_R16 \_ 聖<sup>FNS</sup> (59) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 無的 \_ <sup>電腦</sup> (60) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a>DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a>DXGI_FORMAT_R8 \_ UINT<sup>FNS</sup> (62) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a>DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a>DXGI_FORMAT_R8 \_ 聖<sup>FNS</sup> (64) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 無別 \_ <sup>PCC</sup> (70) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 4 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 4 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FNC</sup> (72) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 4 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 無別 \_ <sup>PCC</sup> (73) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a>DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FNC</sup> (75) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 無別 \_ <sup>PCC</sup> (76) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FNC</sup> (78) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 無別 \_ <sup>PCC</sup> (79) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 4 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 4 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a>DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 4 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 無別 \_ <sup>PCC</sup> (82) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a>DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a>DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 無的 \_ <sup>電腦</sup> (90) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | ![必要](images/letter-r.jpg) |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![必要](images/letter-r.jpg) |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (91) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | ![必要](images/letter-r.jpg) |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![必要](images/letter-r.jpg) |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 無的 \_ <sup>電腦</sup> (92) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | \- |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FNS</sup> (93) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | ![必要](images/letter-r.jpg) |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![必要](images/letter-r.jpg) |
| RenderTarget | ![必要](images/letter-r.jpg) |
| Blendable RenderTarget | ![必要](images/letter-r.jpg) |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 8x 多重採樣 RenderTarget | ![選用](images/letter-o.jpg) |
| 其他的多重採樣計數 RT | ![選用](images/letter-o.jpg) |
| 多級取樣解析 | ![必要](images/letter-r.jpg) |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | ![必要](images/letter-r.jpg) |
| 磚資源 | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 64 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 不 \_ 透明的<sup>V</sup> (106) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | \- |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![必要](images/letter-r.jpg) |
| 視頻處理器輸入 | ![必要](images/letter-r.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 32 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸入 | ![選用](images/letter-o.jpg) |
| 視頻處理器輸出 | ![選用](images/letter-o.jpg) |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![必要](images/letter-r.jpg) |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![必要](images/letter-r.jpg) |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 8 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![必要](images/letter-r.jpg) |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![選用](images/letter-o.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| 著色器範例 (point sample only)  | \- |
| 著色器範例 (任何篩選)  | \- |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | \- |
| Mipmap 自動產生 | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | ![必要](images/letter-r.jpg) |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115) 
| 目標 | 支援 |
| - | - |
| 每個元素的位數 (BPE)  | 16 |
| 格式支援 | ![必要](images/letter-r.jpg) |
| Buffer | \- |
| 輸入組合語言頂點緩衝區 | \- |
| 輸入組合語言索引緩衝區 | \- |
| 資料流程輸出緩衝區 | \- |
| Texture1D | \- |
| Texture2D | ![必要](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![必要](images/letter-r.jpg) |
| 著色器範例 (point sample only)  | ![必要](images/letter-r.jpg) |
| 著色器範例 (任何篩選)  | ![必要](images/letter-r.jpg) |
| 著色 \_ 器範例 c (比較篩選)  | \- |
| 著色器範例 (mono 1 位篩選)  | \- |
| 著色器 gather4 | \- |
| 著色器 gather4 \_ c | \- |
| Mipmap | ![必要](images/letter-r.jpg) |
| Mipmap 自動產生 | ![選用](images/letter-o.jpg) |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| 輸出合併邏輯 Op | \- |
| 深度/樣板目標 | \- |
| 原始 UAV 和 SRV | \- |
| 結構化 UAV 和 SRV | \- |
| 具類型的 UAV | \- |
| UAV 具類型的存放區 | \- |
| UAV 具類型的載入 | \- |
| UAV 不可部分完成的新增 | \- |
| UAV 不可部分完成的位運算 | \- |
| UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name | \- |
| UAV 不可部分完成 Exchange | \- |
| UAV 不可部分完成的帶正負號 Min 或 Max | \- |
| UAV 不可部分完成的不帶正負號 Min 或 Max | \- |
| CPU 鎖定 | ![必要](images/letter-r.jpg) |
| 4x 多重採樣 RenderTarget | \- |
| 8x 多重採樣 RenderTarget | \- |
| 其他的多重採樣計數 RT | \- |
| 多級取樣解析 | \- |
| 多級載入 | \- |
| 顯示 Scan-Out | \- |
| 位配置中的 Cast | \- |
| 影片解碼支援 | \- |
| 視頻處理器輸入 | \- |
| 視頻處理器輸出 | \- |
| 共用資源 | \- |
| 磚資源 | \- |

## <a name="format-notes"></a>格式化附注

格式的用途可從一個硬體功能層級變更為下一個硬體功能層級。

<dl> <dt>

<sup>L</sup> ：無格式的格式
</dt> <dt>

<sup>電腦</sup> ：部分類型、可轉換和簡單版面配置
</dt> <dt>

 <sup>FCS</sup> ：完整型別、可轉換和 simple 版面配置
</dt> <dt>

<sup>FNS</sup> ：完全具類型、非可轉換和簡單版面配置
</dt> <dt>

<sup>PCC</sup> ：部分類型、可轉換和複雜版面配置
</dt> <dt>

 <sup>FCC</sup> ：完整型別、可轉換和複雜的版面配置
</dt> <dt>

<sup>FNC</sup> ：完整型別、非可轉換和複雜的版面配置
</dt> <dt>

<sup>V</sup> ：影片格式
</dt> </dl>

## <a name="related-topics"></a>相關主題

[D3D12 硬體功能等級](../direct3d12/hardware-feature-levels.md)

[針對 Direct3D 功能層級9執行陰影緩衝區](/previous-versions/windows/apps/jj262110(v=win.10))

[對應舊版格式](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
