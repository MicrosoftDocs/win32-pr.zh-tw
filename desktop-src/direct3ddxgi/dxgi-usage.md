---
description: 介面和資源建立選項的旗標。
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: 'DXGI_USAGE (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976700"
---
# <a name="dxgi_usage"></a>DXGI \_ 使用量

介面和資源建立選項的旗標。



| 常數/值                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_使用量 \_ 回 \_ 緩衝區**</dt> <dt>1L <<  (2 + 4)</dt> </dl>                             | 介面或資源會用來做為背景緩衝區。 當您建立交換鏈時，不需要將 **DXGI 的 \_ 使用方式傳遞 \_ 回 \_ 緩衝區** 。 但是，您可以在呼叫 [**IDXGIResource：： GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) 並取得 **DXGI \_ 使用方式 \_ \_ 緩衝區** 時，判斷資源是否屬於交換鏈。<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_\_ \_ 在 \_ 目前的1L 上使用捨棄**</dt> <dt> <<  (5 + 4)</dt> </dl>       | 此旗標僅供內部使用。<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_使用 \_ 唯讀 \_**</dt> <dt>1L <<  (4 + 4)</dt> </dl>                                   | 使用介面或資源僅供讀取。<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_使用方式 \_ 呈現 \_ 目標 \_ 輸出**</dt> <dt>1L <<  (1 + 4)</dt> </dl> | 使用介面或資源作為輸出呈現目標。<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_使用 \_ 著色器 \_ 輸入**</dt> <dt>1L <<  (0 + 4)</dt> </dl>                          | 使用介面或資源做為著色器的輸入。<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_使用量 \_ 共用**</dt> <dt>1L <<  (3 + 4)</dt> </dl>                                             | 共用 surface 或資源。<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_使用未 \_ 排序 \_ 存取**</dt> <dt>1L <<  (6 + 4)</dt> </dl>              | 使用介面或資源進行未排序的存取。<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>備註

每個旗標都會定義為不帶正負號的整數。

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

在呼叫 [**IDXGIFactory：： CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain)、 [**IDXGIFactory2：： CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)、 [**IDXGIFactory2：： CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)或 [**IDXGIFactory2：： CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) 方法時，會使用這些旗標選項來描述交換鏈背面緩衝區的介面使用狀況和 CPU 存取選項。 您無法使用 [ **dxgi \_ \_ 共用**]、[ **dxgi 使用方式 \_ \_ \_ \_ 捨棄**] 和 [ **dxgi \_ 使用 \_ 唯讀 \_** ] 值做為輸入來建立交換鏈。 不過，DXGI 可以 **\_ \_ \_ 在 \_ 目前的情況下設定 dxgi 使用方式捨棄** ，而在應用程式上，對某些交換鏈的背景緩衝區進行 **\_ \_ 唯讀 \_ 使用** 。 您可以呼叫 [**IDXGIResource：： GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) 方法來取得這些背景緩衝區的使用方式。 交換鏈在 **dxgi \_ 使用量** 的 [ **dxgi \_ cpu \_ 存取] \_ 欄位** 部分中，僅支援 [ **dxgi \_ cpu \_ 存取 \_ 無**] 值。

[**IDXGIDevice：： CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface)方法也會使用這些旗標選項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DXGI。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 常數](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




