---
description: 指定要在受保護的視頻界面中加密的位元組。
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: 'D3DENCRYPTED_BLOCK_INFO 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111801"
---
# <a name="d3dencrypted_block_info-structure"></a>D3DENCRYPTED \_ 區塊 \_ 資訊結構

指定要在受保護的視頻界面中加密的位元組。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**NumEncryptedBytesAtBeginning**
</dt> <dd>

在緩衝區開頭加密的位元組數目。

</dd> <dt>

**NumBytesInSkipPattern**
</dt> <dd>

在第一個 **NumEncryptedBytesAtBeginning** 的位元組之後，以及每個 **NumBytesInEncryptPattern** 位元組區塊之後略過的位元組數目。 略過的位元組不會加密。

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

在每個略過的位元組區塊之後加密的位元組數目。

</dd> </dl>

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

 

 




