---
description: 本主題說明適用于各種版本 Windows 10 的 Microsoft DirectX Graphic Infrastructure (DXGI) 1.6 中的新功能。
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: DXGI 1.6 改進
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 03961b4f9af50675ee157c4840b9ed744c54f423
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510257"
---
# <a name="dxgi-16-improvements"></a>DXGI 1.6 改進

本主題說明適用于各種版本 Windows 10 的 Microsoft DirectX Graphic Infrastructure (DXGI) 1.6 中的新功能。

## <a name="windows-10-october-2018-update"></a>Windows 10 2018 年 10 月更新

這些 Api 已新增至 Windows 10 版本 1809 (10.0;組建 17763) &mdash; 也稱為 Windows 10 2018 年10月更新。

- [**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) 介面和其方法。

## <a name="windows-10-april-2018-update"></a>Windows 10 2018 4 月更新

這些 Api 已針對 Windows 10，1803版 (10.0;組建 17134) &mdash; 也稱為 Windows 10 2018 年4月更新。

- [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) 列舉。
- [**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) 介面和其方法。

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

若為 Windows 10，1709版 (10.0;組建 16299) &mdash; 也稱為 Windows 10 Fall Creators Update &mdash; 這些常數已新增至 [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) 列舉。 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

若為 Windows 10，1703版 (10.0;組建 15063) &mdash; 也稱為 Windows 10 Creators Update &mdash; 下列功能已新增至 Microsoft DIRECTX GRAPHIC INFRASTRUCTURE (DXGI) 1.6 以偵測 HDR 顯示器。

### <a name="high-dynamic-range-hdr-detection"></a>高動態範圍 (HDR) 偵測

新增這些 Api 是為了偵測 HDR 顯示。

- [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3) 結構
- [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) 列舉
- [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags) 列舉
- [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) 結構
- [**DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport) 函式
- [**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) 介面及其方法
- [**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) 介面及其方法

此外，常數也已新增至 [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) 列舉，以支援這些 api。

## <a name="related-topics"></a>相關主題
[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
