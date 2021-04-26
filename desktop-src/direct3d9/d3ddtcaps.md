---
description: 描述裝置所支援之頂點資料類型的常數。
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 094ca568554722f4da2606233f4ad2c1e59e892f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999445"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

描述裝置所支援之頂點資料類型的常數。



| \#定義              | 值       | 描述                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | 4D 不帶正負號的位元組。                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | 正規化、4D 不帶正負號的位元組。 四個位元組的每一個都是除以255.0 來正規化。                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | 正規化、2D 帶正負號的簡短，展開為 (第一個位元組/32767.0，第二個位元組/32767.0，0，1) 。                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | 正規化、4D 帶正負號的簡短，展開為 (第一個位元組/32767.0，第二個位元組/32767.0，第三個位元組/32767.0，第四個位元組/32767.0) 。  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | 正規化、2D 不帶正負號的短，展開為 (第一個位元組/65535.0，第二個位元組/65535.0，0，1) 。                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020L | 正規化的4D 不帶正負號短，展開為 (第一個位元組/65535.0，第二個位元組/65535.0，第三個位元組/65535.0，第四個位元組/65535.0) 。 |
| D3DDTCAPS \_ UDEC3      | 0x00000040L | 3D 未簽署的 10 10 10 格式會展開為 (值、值、值、1) 。                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080L | 以3D 簽署的 10 10 10 格式正規化和展開為 (v \[ 0 \] /511.0、v \[ 1 \] /511.0、v \[ 2 \] /511.0、1) 。                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | 2D 16 位浮點數。                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | 4D 16 位浮點數。                                                                                             |



 

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 DeclTypes 成員會使用這些常數。

## <a name="constant-information"></a>常數資訊



|                          |            |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



