---
description: 包含對 IDirect3DAuthenticatedChannel9：： Configure 方法之呼叫的回應。
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317991"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸出結構

包含對 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 方法之呼叫的回應。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
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

已驗證通道的控制碼。

</dd> <dt>

**SequenceNumber**
</dt> <dd>

命令的序號。

</dd> <dt>

**ReturnCode**
</dt> <dd>

命令的結果碼。

</dd> </dl>

## <a name="remarks"></a>備註

針對 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員，驅動程式會使用 [**D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構中所提供的相同值。 應用程式應該驗證這些值是否相符。

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

 

 




