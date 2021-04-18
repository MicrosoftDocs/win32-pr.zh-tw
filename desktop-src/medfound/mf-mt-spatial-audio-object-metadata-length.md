---
description: 值，指定解碼器將輸出的空間音訊中繼資料物件類型大小（以位元組為單位）。
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: 'MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193015"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a><span data-ttu-id="b8cc2-103">MF \_ MT \_ 空間 \_ 音訊 \_ 物件 \_ 中繼資料 \_ 長度屬性</span><span class="sxs-lookup"><span data-stu-id="b8cc2-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_LENGTH attribute</span></span>

<span data-ttu-id="b8cc2-104">值，指定解碼器將輸出的空間音訊中繼資料物件類型大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b8cc2-104">A value specifying the size, in bytes, of the spatial audio metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8cc2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b8cc2-105">Data type</span></span>

<span data-ttu-id="b8cc2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b8cc2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cc2-107">備註</span><span class="sxs-lookup"><span data-stu-id="b8cc2-107">Remarks</span></span>

<span data-ttu-id="b8cc2-108">使用 [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) 介面寫入具有指定格式的中繼資料 blob，並使用 [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) 介面進行讀取。</span><span class="sxs-lookup"><span data-stu-id="b8cc2-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="b8cc2-109">中繼資料 blob 對媒體基礎管線和元件而言是不透明的。</span><span class="sxs-lookup"><span data-stu-id="b8cc2-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="b8cc2-110">屬性會套用至空間音訊媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b8cc2-110">The attribute is applied to the spatial audio media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8cc2-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8cc2-111">Requirements</span></span>



| <span data-ttu-id="b8cc2-112">需求</span><span class="sxs-lookup"><span data-stu-id="b8cc2-112">Requirement</span></span> | <span data-ttu-id="b8cc2-113">值</span><span class="sxs-lookup"><span data-stu-id="b8cc2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cc2-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8cc2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cc2-115">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8cc2-115">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b8cc2-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8cc2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cc2-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="b8cc2-117">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b8cc2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b8cc2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8cc2-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8cc2-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
