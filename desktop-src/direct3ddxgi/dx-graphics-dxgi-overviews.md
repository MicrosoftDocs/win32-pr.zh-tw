---
description: Microsoft DirectX Graphic Infrastructure (DXGI) 管理可獨立于 Direct3D 圖形執行時間之外的低層級工作。 DXGI 提供數個 Direct3D 版本的通用架構。
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: DXGI 的程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7834b2fc68019dccfb8ab8b2e62698465ff1ea2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187404"
---
# <a name="programming-guide-for-dxgi"></a>DXGI 的程式設計指南

Microsoft DirectX Graphic Infrastructure (DXGI) 管理可獨立于 Direct3D 圖形執行時間之外的低層級工作。 DXGI 提供數個 Direct3D 版本的通用架構。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                              | 描述                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DXGI 總覽](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | 本主題包含下列各節。<br/>                                                                                                                   |
| [DXGI 1.2 改進](dxgi-1-2-improvements.md)<br/>                                                                      | 已在 DXGI 1.2 中新增下列功能。<br/>                                                                                                       |
| [DXGI 1.3 改進](dxgi-1-3-improvements.md)<br/>                                                                      | 已在 DXGI 1.3 中新增下列功能，此功能已在 Windows 8.1 中提供。<br/>                                                            |
| [DXGI 1.4 改進](dxgi-1-4-improvements.md)<br/>                                                                      | 在 DXGI 1.4 中新增或變更了下列功能，主要是為了支援 Direct3D 12。 <br/>                                                           |
| [DXGI 1.5 改進](dxgi-1-5-improvements.md)<br/>                                                                      | 下列功能已新增至 DXGI 1.5，以支援更具彈性的指定和複製輸出格式。<br/>                                |
| [DXGI 1.6 改進](dxgi-1-6-improvements.md)<br/>                                                                      | 下列功能已新增至 DXGI 1.6，以便偵測 HDR 顯示。<br/>                                                                       |
| [使用 DirectX 搭配高動態範圍顯示和進階色彩](../direct3darticles/high-dynamic-range.md)     | 本主題提供使用 Windows 10 advanced color support 將高動態範圍 Direct3D 11 和 Direct3D 12 內容轉譯為 HDR10 顯示的技術總覽。<br/> |
| [變數重新整理率顯示](variable-refresh-rate-displays.md)<br/>                                                    | 變數重新整理率顯示 *需要卸載* 才能啟用，這也稱為「vsync 關閉」支援。<br/>                                                    |
| [使用 gamma 更正](using-gamma-correction.md)<br/>                                                                    | Gamma 更正（簡稱為 gamma）是指系統用來編碼和解碼影像中圖元值的非線性運算名稱。<br/>                        |
| [Direct3D Feature 10Level9 9.1 硬體的格式支援](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | 此區段會指定 Direct3D Feature 10Level9 9.1 硬體支援的格式 ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值) 。<br/>        |
| [Direct3D Feature 10Level9 9.3 硬體的格式支援](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | 此區段會指定 Direct3D Feature 10Level9 9.3 硬體支援的格式 ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值) 。<br/>        |
| [Direct3D 功能等級10.0 硬體的格式支援](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | 此區段會指定 Direct3D 10.0 硬體中所支援)  ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值的格式。<br/>                        |
| [Direct3D 功能等級10.1 硬體的格式支援](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | 此區段會指定 Direct3D 10.1 硬體中所支援)  ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值的格式。<br/>                        |
| [Direct3D 功能等級11.0 硬體的格式支援](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | 此區段會指定 Direct3D 功能等級11.0 硬體支援的格式 ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值) 。<br/>          |
| [Direct3D 功能等級11.1 硬體的格式支援](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | 此區段會指定 Direct3D 功能等級11.1 硬體支援的格式 ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值) 。<br/>          |
| [Direct3D 功能等級12.0 硬體的格式支援](hardware-support-for-direct3d-12-0-formats.md)<br/>               | 此區段會指定 Direct3D 功能等級12.0 硬體支援的格式 ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值) 。<br/>          |
| [Direct3D 功能等級12.1 硬體的格式支援](hardware-support-for-direct3d-12-1-formats.md)<br/>               | 此區段會指定 Direct3D 12.1 硬體中所支援)  ([**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值的格式。<br/>                        |
| [檢查硬體功能支援](checking-hardware-feature-support.md)<br/>                                              | 本節涵蓋如何使用 API 呼叫來檢查 Direct3D 功能等級硬體的格式支援。<br/>                                                       |
| [為了達到最佳效能，請使用 DXGI 翻轉模型](for-best-performance--use-dxgi-flip-model.md)<br/>                              | 本主題提供開發人員指引，說明如何在新式 Windows 的簡報堆疊中最大化效能和效率。<br/>                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[DXGI 參考](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[DirectX Graphic Infrastructure (DXGI) ：最佳作法](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
