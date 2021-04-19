---
description: 包含 D3DAUTHENTICATEDCONFIGURE CRYPTOSESSION 命令的輸入資料 \_ 。
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973196"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION 結構

包含 [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) 命令的輸入資料。

若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a>成員

<dl> <dt>

**參數**
</dt> <dd>

D3DAUTHENTICATEDCHANNEL 設定包含命令 GUID 和其他資料的 [**\_ \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構。

</dd> <dt>

**DXVA2DecodeHandle**
</dt> <dd>

DirectX Video 加速 2 (DXVA-2) 解碼器裝置的控制碼。

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

密碼編譯會話的控制碼。

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Direct3D 裝置的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片結構](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




