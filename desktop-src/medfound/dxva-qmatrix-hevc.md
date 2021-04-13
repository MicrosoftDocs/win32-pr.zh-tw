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
# <a name="dxva_qmatrix_hevc-structure"></a><span data-ttu-id="ec78a-103">DXVA \_ Qmatrix \_ HEVC 結構</span><span class="sxs-lookup"><span data-stu-id="ec78a-103">DXVA\_Qmatrix\_HEVC structure</span></span>

<span data-ttu-id="ec78a-104">定義量化矩陣。</span><span class="sxs-lookup"><span data-stu-id="ec78a-104">Defines a quantization matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec78a-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec78a-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="ec78a-106">成員</span><span class="sxs-lookup"><span data-stu-id="ec78a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec78a-107">**ucScalingLists0 \[ 6 \] \[ 16\]**</span><span class="sxs-lookup"><span data-stu-id="ec78a-107">**ucScalingLists0\[6\]\[16\]**</span></span>
</dt> <dd>

<span data-ttu-id="ec78a-108">包含4x4 調整程式的縮放清單，對應于 HEVC 規格中的 ScalingList \[ 0 \] \[ MatrixID \] \[ i， \] 其中 MatrixID 是在0到5（含）的範圍內，而我的範圍介於0到15（含）之間。</span><span class="sxs-lookup"><span data-stu-id="ec78a-108">Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList\[ 0 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="ec78a-109">**ucScalingLists1 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="ec78a-109">**ucScalingLists1\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="ec78a-110">包含8x8 調整程式的縮放清單（對應至 HEVC 規格中的 ScalingList \[ 1 \] \[ MatrixID \] \[ i） \] ，其中 MatrixID 是在0到5（含）的範圍內，而 i 是介於0到63（含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="ec78a-110">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 1 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="ec78a-111">**ucScalingLists2 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="ec78a-111">**ucScalingLists2\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="ec78a-112">包含8x8 調整程式的縮放清單（對應至 HEVC 規格中的 ScalingList \[ 2 \] \[ MatrixID \] \[ i） \] ，其中 MatrixID 是在0到5（含）的範圍內，而 i 是介於0到63（含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="ec78a-112">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 2 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="ec78a-113">**ucScalingLists3 \[ 2 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="ec78a-113">**ucScalingLists3\[2\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="ec78a-114">包含8x8 調整程式的縮放清單（對應至 HEVC 規格中的 ScalingList \[ 3 \] \[ MatrixID i）， \] \[ \] 其中 MatrixID 的範圍介於0到1（含）之間，而 i 的範圍介於0到63（含）之間。</span><span class="sxs-lookup"><span data-stu-id="ec78a-114">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 3 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="ec78a-115">**ucScalingListDCCoefSizeID2**</span><span class="sxs-lookup"><span data-stu-id="ec78a-115">**ucScalingListDCCoefSizeID2**</span></span>
</dt> <dd>

<span data-ttu-id="ec78a-116">包含 sizeID 等於2且對應至縮放 \_ 清單 \_ dc \_ coef \_ minus8 \[ sizeID − 2 matrixID + 8、sizeID 等於2的縮放清單 dc 值，以及 matrixID \] \[ \] 規格中0到5（含）範圍內的 HEVC。</span><span class="sxs-lookup"><span data-stu-id="ec78a-116">Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification.</span></span>

</dd> <dt>

<span data-ttu-id="ec78a-117">**ucScalingListDCCoefSizeID3**</span><span class="sxs-lookup"><span data-stu-id="ec78a-117">**ucScalingListDCCoefSizeID3**</span></span>
</dt> <dd>

<span data-ttu-id="ec78a-118">包含 sizeID 等於3之32x32 大小的縮放清單的 DC 值，而且對應至縮放 \_ 清單 \_ dc \_ coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8，sizeID 等於3，而 matrixID 的範圍介於0到1（含）的 HEVC 規格中。</span><span class="sxs-lookup"><span data-stu-id="ec78a-118">Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec78a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec78a-119">Requirements</span></span>



| <span data-ttu-id="ec78a-120">需求</span><span class="sxs-lookup"><span data-stu-id="ec78a-120">Requirement</span></span> | <span data-ttu-id="ec78a-121">值</span><span class="sxs-lookup"><span data-stu-id="ec78a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ec78a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec78a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ec78a-123">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec78a-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ec78a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec78a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ec78a-125">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec78a-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ec78a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ec78a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec78a-127"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec78a-127"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec78a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec78a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec78a-129">媒體基礎結構</span><span class="sxs-lookup"><span data-stu-id="ec78a-129">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




