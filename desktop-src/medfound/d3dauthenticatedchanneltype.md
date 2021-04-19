---
description: 指定 Direct3D 驗證通道的類型。
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: 'D3DAUTHENTICATEDCHANNELTYPE 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971982"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a>D3DAUTHENTICATEDCHANNELTYPE 列舉

指定 Direct3D 驗證通道的類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ D3D9**
</dt> <dd>

Direct3D 9 通道。 此通道會提供與 Direct3D 執行時間的通訊。

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**
</dt> <dd>

軟體驅動程式通道。 此通道提供的驅動程式與在軟體中實施內容保護機制的驅動程式通訊。

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**
</dt> <dd>

硬體驅動程式通道。 此通道可讓您與驅動程式進行通訊，以在 GPU 硬體中執行內容保護機制。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>D3d9types (包含 D3d9) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片列舉](direct3d-video-enumerations.md)
</dt> <dt>

[**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




