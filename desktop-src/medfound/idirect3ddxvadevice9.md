---
description: 代表 DirectX Video 加速的硬體加速器 (DXVA) 1.0。
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: 'IDirect3DDXVADevice9 介面 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974408"
---
# <a name="idirect3ddxvadevice9-interface"></a>IDirect3DDXVADevice9 介面

代表 DirectX Video 加速的硬體加速器 (DXVA) 1.0。

## <a name="members"></a>成員

**IDirect3DDXVADevice9** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDirect3DDXVADevice9** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirect3DDXVADevice9** 介面具有這些方法。



| 方法                                                  | 描述                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**BeginFrame**](idirect3ddxvadevice9-beginframe.md)   | 開始處理以建立解碼的圖片。<br/>         |
| [**EndFrame**](idirect3ddxvadevice9-endframe.md)       | 結束處理以建立解碼的圖片。<br/>           |
| [**執行**](idirect3ddxvadevice9-execute.md)         | 執行 DXVA 解碼作業。 <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | 查詢 DXVA 解碼介面的讀取/寫入狀態。 <br/> |



 

## <a name="remarks"></a>備註

若要取得這個介面的指標，請呼叫 [**IDirect3DVideoDevice9：： CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D Video 介面](direct3d-video-interfaces.md)
</dt> </dl>

 

 
