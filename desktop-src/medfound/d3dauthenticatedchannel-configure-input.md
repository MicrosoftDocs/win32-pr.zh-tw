---
description: 包含 IDirect3DAuthenticatedChannel9：： Configure 方法的輸入資料。
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: de968c83fee7ae68dcd756bdf83d529593eeb30b3c2776b03cda812bcd442c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974737"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸入結構

包含 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 方法的輸入資料。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**omac**
</dt> <dd>

[**D3D \_ OMAC**](d3d-omac.md)結構，其中包含資料的訊息驗證碼 (MAC) 。 驅動程式會使用 AES 型單鍵 CBC MAC (OMAC) 為此結構成員後面出現的資料區塊計算此值。

</dd> <dt>

**ConfigureType**
</dt> <dd>

指定命令的 GUID。 如需值的清單，請參閱 [內容保護命令](content-protection-commands.md)。

</dd> <dt>

**hChannel**
</dt> <dd>

已驗證通道的控制碼。 若要取得控制碼，請呼叫 [**IDirect3DDevice9Video：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)。

</dd> <dt>

**SequenceNumber**
</dt> <dd>

查詢序號。 在會話開始時，產生以密碼編譯的安全32位亂數字，作為起始序號使用。 針對每個命令，將序號遞增1。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片結構](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




