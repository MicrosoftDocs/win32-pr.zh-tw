---
title: 磚資源建立參數
description: 您可以使用 D3D11 資源其他並排顯示旗標建立的 Direct3D 資源類型有一些 \_ 限制 \_ \_ 。 本節提供用來建立磚資源的有效參數。
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9668c21060cbb8f39884204780ce689b3e67196aef0bdcfef891836768f04af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279838"
---
# <a name="tiled-resource-creation-parameters"></a>磚資源建立參數

您可以使用 [**D3D11 \_ 資源 \_ 其他 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) 並排顯示旗標建立的 Direct3D 資源類型有一些限制。 本節提供用來建立磚資源的有效參數。

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**支援的資源類型**
</dt> <dd>

Texture2D \[ 陣列 \] (包括 TextureCube \[ 陣列 \] ，這是 Texture2D \[ 陣列 \]) 或緩衝區的變異。

**不支援：** Texture1D \[ 陣列 \] 或 Texture3D，但未來可能會支援 Texture3D。

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**支援的資源使用方式**
</dt> <dd>

D3D11 \_ 使用 \_ 預設值。

**不支援：** D3D11 \_ 使用 \_ 動態、D3D11 \_ 使用 \_ 暫存或 D3D11 \_ 使用量 \_ 不可變。

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**支援的資源其他旗標**
</dt> <dd>

D3D11 \_ \_ \_ 由定義) 、 \_ 其他 \_ TEXTURECUBE、DRAWINDIRECT 引數 \_ \_ 、 \_ 緩衝區 \_ 允許 \_ 原始 \_ 的視圖、 \_ 緩衝區 \_ 結構化、 \_ 資源資源區 \_ ，或 \_ 產生 \_ MIPS 的資源其他 (並排顯示的。

**不支援：** \_共用、 \_ 共用 \_ KEYEDMUTEX、 \_ GDI \_ 相容、 \_ 共用 \_ NTHANDLE、 \_ 受限 \_ 的內容、 \_ 限制 \_ 共用 \_ 資源、 \_ 限制 \_ 共用 \_ 資源 \_ 驅動程式、受防護 \_ 或 \_ 磚集區 \_ 。

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**支援的系結旗標**
</dt> <dd>

D3D11 系結 \_ \_ 著色器 \_ 資源、轉譯 \_ \_ 目標、 \_ 深度樣板或未 \_ \_ 排序 \_ 的存取。

**不支援：** \_常數 \_ 緩衝區、 \_ 頂點緩衝區附注，將並排緩衝區系結 \_ \[ 為 SRV/UAV/RTV 仍然是正常的 \] 、 \_ 索引 \_ 緩衝區、 \_ 串流輸出、系結解碼器或系結 \_ \_ \_ \_ \_ 影片 \_ 編碼器。

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**支援的格式**
</dt> <dd>

特定設定的所有格式 (不管它是區塊式)，但有一些例外。

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**支援的 SampleDesc (的高取樣計數、品質)**
</dt> <dd>

特定設定的所有描述都會受支援 (不管它是區塊式)，但有一些例外。

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**支援的寬度/高度/MipLevels/ArraySize**
</dt> <dd>

Direct3D 11 支援的完整範圍。 並排顯示的資源並不會限制非並排顯示資源上的總記憶體大小。 磚的資源只會受到整體虛擬位址空間限制的限制。 如需詳細資訊，請參閱 [適用于並排資源的位址空間](address-space-available-for-tiled-resources.md)。

</dd> </dl>

磚集區記憶體的初始內容未定義。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立磚資源](creating-tiled-resources.md)
</dt> </dl>

 

 




