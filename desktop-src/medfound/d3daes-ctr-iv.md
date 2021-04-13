---
description: 包含128位進階加密標準 CTR 模式 (CTR) 區塊加密加密 (IV) 的初始化向量。
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: 'D3DAES_CTR_IV 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317992"
---
# <a name="d3daes_ctr_iv-structure"></a>D3DAES \_ CTR \_ IV 結構

包含128位進階加密標準 CTR 模式 (CTR) 區塊加密加密 (IV) 的初始化向量。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>成員

<dl> <dt>

**IV**
</dt> <dd>

以位元組由大到小的格式的 IV。

</dd> <dt>

**Count**
</dt> <dd>

以位元組由大到小的格式的區塊計數。

</dd> </dl>

## <a name="remarks"></a>備註

**D3DAES \_ CTR \_ Iv** 結構和 [**DXVA2 \_ AES \_ CTR \_ iv**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv)結構是相等的。

如需詳細資訊，請參閱 [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>D3d9types (包含 D3d9) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片結構](direct3d-video-structures.md)
</dt> </dl>

 

 




