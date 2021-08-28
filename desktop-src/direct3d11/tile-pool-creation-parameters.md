---
title: 磚集區建立參數
description: 使用本節中的參數，透過 ID3D11Device CreateBuffer API 定義磚集區。
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7350dc01c845542b97674189a120c0d55db95c282dc80b11fda66230618f99b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119468"
---
# <a name="tile-pool-creation-parameters"></a>磚集區建立參數

使用本節中的參數透過 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API 定義磚集區。

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**大小**
</dt> <dd>

配置大小需為 64 KB 的倍數 0有效，因為您稍後可以使用 [**ID3D11DeviceCoNtext2：： ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) 作業。

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**支援的資源其他旗標**
</dt> <dd>

D3D11 \_ 資源 \_ 其他 \_ 磚 \_ 集區 (將資源識別為磚集區) 、D3D11 \_ 資源 \_ 其他 \_ 共用、 \_ 共用 \_ KEYEDMUTEX 或 \_ 共用 \_ NTHANDLE。

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**支援的資源使用方式**
</dt> <dd>

D3D11 \_ 使用 \_ 預設值。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立磚資源](creating-tiled-resources.md)
</dt> </dl>

 

 




