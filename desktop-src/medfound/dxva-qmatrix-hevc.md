---
description: 定義量化矩陣。
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: 'DXVA_Qmatrix_HEVC 結構 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510798"
---
# <a name="dxva_qmatrix_hevc-structure"></a>DXVA \_ Qmatrix \_ HEVC 結構

定義量化矩陣。

## <a name="syntax"></a>語法


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a>成員

<dl> <dt>

**ucScalingLists0 \[ 6 \] \[ 16\]**
</dt> <dd>

包含4x4 調整程式的縮放清單，對應于 HEVC 規格中的 ScalingList \[ 0 \] \[ MatrixID \] \[ i， \] 其中 MatrixID 是在0到5（含）的範圍內，而我的範圍介於0到15（含）之間。

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

包含8x8 調整程式的縮放清單（對應至 HEVC 規格中的 ScalingList \[ 1 \] \[ MatrixID \] \[ i） \] ，其中 MatrixID 是在0到5（含）的範圍內，而 i 是介於0到63（含）的範圍內。

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

包含8x8 調整程式的縮放清單（對應至 HEVC 規格中的 ScalingList \[ 2 \] \[ MatrixID \] \[ i） \] ，其中 MatrixID 是在0到5（含）的範圍內，而 i 是介於0到63（含）的範圍內。

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

包含8x8 調整程式的縮放清單（對應至 HEVC 規格中的 ScalingList \[ 3 \] \[ MatrixID i）， \] \[ \] 其中 MatrixID 的範圍介於0到1（含）之間，而 i 的範圍介於0到63（含）之間。

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

包含 sizeID 等於2且對應至縮放 \_ 清單 \_ dc \_ coef \_ minus8 \[ sizeID − 2 matrixID + 8、sizeID 等於2的縮放清單 dc 值，以及 matrixID \] \[ \] 規格中0到5（含）範圍內的 HEVC。

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

包含 sizeID 等於3之32x32 大小的縮放清單的 DC 值，而且對應至縮放 \_ 清單 \_ dc \_ coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8，sizeID 等於3，而 matrixID 的範圍介於0到1（含）的 HEVC 規格中。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎結構](media-foundation-structures.md)
</dt> </dl>

 

 




