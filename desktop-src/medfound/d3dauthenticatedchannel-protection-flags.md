---
description: 指定影片內容的保護層級。
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: 'D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1d1b76a6fea0dd6b966bd72001efb187a7a3a14e75b4d41d631e5a1ea163fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974707"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>D3DAUTHENTICATEDCHANNEL \_ 保護 \_ 旗標結構

指定影片內容的保護層級。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a>成員

<dl> <dt>

**ProtectionEnabled**
</dt> <dd>

若為1，則會啟用影片內容保護。

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

如果是1，則應用程式需要使用硬體重迭或全螢幕獨佔模式來顯示影片。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。 將所有位設為零。

</dd> <dt>

**值**
</dt> <dd>

您可以使用這個成員來存取等位中的所有位。

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
</dt> </dl>

 

 




