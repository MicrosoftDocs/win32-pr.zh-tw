---
description: 包含 D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE 命令的輸入資料 \_ 。
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 0dbff67921f2ec6ad634c20b11b86b0384923db5548bcef113128fe5ede6bdd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742904"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE 結構

包含 [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) 命令的輸入資料。

若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a>成員

<dl> <dt>

**參數**
</dt> <dd>

D3DAUTHENTICATEDCHANNEL 設定包含命令 GUID 和其他資料的 [**\_ \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構。

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

指定進程類型的 [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) 值。 若要指定桌面視窗管理員 (DWM) 進程，請將這個成員設定為 **PROCESSIDTYPE \_ dwm**。 否則，請將這個成員設定為 **PROCESSIDTYPE \_ 控制碼** ，並將 **ProcessHandle** 成員設定為有效的控制碼。

</dd> <dt>

**ProcessHandle**
</dt> <dd>

進程控制碼。 如果 **ProcessIdentifier** 成員等於 **PROCESSTIDTYPE \_ 控制碼**， **ProcessHandle** 成員會指定進程的控制碼。 否則會忽略此值。

</dd> <dt>

**AllowAccess**
</dt> <dd>

若 **為 TRUE**，表示指定的進程可以存取受限制的共用資源。

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

 

 




