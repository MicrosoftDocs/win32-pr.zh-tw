---
description: 列舉顯示模式的選項。
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: 'DXGI_ENUM_MODES (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992309"
---
# <a name="dxgi_enum_modes"></a>DXGI \_ 列舉 \_ 模式

列舉顯示模式的選項。



| 常數/值                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**DXGI \_列舉 \_ 模式 \_ 交錯**</dt>式 <dt>1UL</dt> </dl>                 | 包含交錯模式。<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**DXGI \_列舉 \_ 模式 \_ 調整**</dt> <dt>2UL</dt> </dl>                          | 包含延伸調整模式。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**DXGI \_列舉 \_ 模式 \_ 身歷聲**</dt> <dt>4UL</dt> </dl>                             | 包含身歷聲模式。<br/> **Direct3D 11：** 從 Windows 8 開始支援這個列舉值。<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**DXGI \_\_ \_ 已停用 \_ 的列舉模式身歷聲**</dt> <dt>8UL</dt> </dl> | 包含因為使用者已停用身歷聲而隱藏的立體模式。 [控制台] 應用程式可以使用此選項，顯示在啟用和停用身歷聲的使用者介面中，已停用的立體功能。<br/> **Direct3D 11：** 從 Windows 8 開始支援這個列舉值。<br/> |



## <a name="remarks"></a>備註

[**IDXGIOutput：： GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist)中使用這些旗標選項來列舉顯示模式。

[**IDXGIOutput1：： GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)也會使用這些旗標選項來列舉顯示模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DXGI。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 常數](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




