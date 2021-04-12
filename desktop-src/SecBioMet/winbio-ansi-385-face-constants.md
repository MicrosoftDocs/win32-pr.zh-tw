---
title: 'WINBIO_ANSI_385_FACE 常數 (Winbio \_ 類型 .h) '
description: 指定臉部辨識的正面臉部影像類型。
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105413"
---
# <a name="winbio_ansi_385_face-constants"></a><span data-ttu-id="7c1e4-103">WINBIO \_ ANSI \_ 385 \_ 臉部常數</span><span class="sxs-lookup"><span data-stu-id="7c1e4-103">WINBIO\_ANSI\_385\_FACE Constants</span></span>

<span data-ttu-id="7c1e4-104">下列常數是 **WINBIO \_ 生物特徵 \_ 子** 型別值，可用來指定 ANSI INCITS 385-2004 所定義的兩種正面臉部影像：「資料交換的臉部辨識格式」：完整解析度和低解析度。</span><span class="sxs-lookup"><span data-stu-id="7c1e4-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the two types of frontal face images as defined by ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": full resolution and low resolution.</span></span> <span data-ttu-id="7c1e4-105">在實務上，生物特徵辨識架構只會使用完整的解析度影像進行臉部辨識。</span><span class="sxs-lookup"><span data-stu-id="7c1e4-105">In practice, the biometric framework will use only full resolution images for facial recognition.</span></span>



| <span data-ttu-id="7c1e4-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="7c1e4-106">Constant/value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="7c1e4-107">Description</span><span class="sxs-lookup"><span data-stu-id="7c1e4-107">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <span data-ttu-id="7c1e4-108"><dt>**WINBIO \_ANSI \_ 385 \_ 臉部 \_ 類型 \_ 未知**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c1e4-108"><dt>**WINBIO\_ANSI\_385\_FACE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="7c1e4-109">正面臉部影像類型未知。</span><span class="sxs-lookup"><span data-stu-id="7c1e4-109">The frontal face image type is unknown.</span></span><br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <span data-ttu-id="7c1e4-110"><dt>**WINBIO \_ANSI \_ 385 \_ 臉部 \_ 正面 \_ FULL**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7c1e4-110"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_FULL**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="7c1e4-111">正面臉部影像類型為完整解析度。</span><span class="sxs-lookup"><span data-stu-id="7c1e4-111">The frontal face image type is full resolution.</span></span><br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <span data-ttu-id="7c1e4-112"><dt>**WINBIO \_ANSI \_ 385 \_ 臉部 \_ 正面 \_ 權杖**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7c1e4-112"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_TOKEN**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7c1e4-113">正面臉部影像類型為低解析度。</span><span class="sxs-lookup"><span data-stu-id="7c1e4-113">The frontal face image type is low resolution.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="7c1e4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c1e4-114">Requirements</span></span>



| <span data-ttu-id="7c1e4-115">需求</span><span class="sxs-lookup"><span data-stu-id="7c1e4-115">Requirement</span></span> | <span data-ttu-id="7c1e4-116">值</span><span class="sxs-lookup"><span data-stu-id="7c1e4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1e4-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c1e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1e4-118">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c1e4-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7c1e4-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c1e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1e4-120">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c1e4-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7c1e4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7c1e4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c1e4-122"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7c1e4-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





