---
description: 用來識別空間音訊元資料格式的解碼器定義 GUID，會通知中繼資料物件類型的下游元件，該型別會輸出該解碼器。
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: 'MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193016"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a><span data-ttu-id="9b5ef-103">MF \_ MT \_ 空間 \_ 音訊 \_ 物件 \_ 中繼資料 \_ 格式 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="9b5ef-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_FORMAT\_ID attribute</span></span>

<span data-ttu-id="9b5ef-104">用來識別空間音訊元資料格式的解碼器定義 GUID，會通知中繼資料物件類型的下游元件，該型別會輸出該解碼器。</span><span class="sxs-lookup"><span data-stu-id="9b5ef-104">A decoder-defined GUID that identifies the spatial audio metadata format, notifying downstream components of the metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b5ef-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9b5ef-105">Data type</span></span>

<span data-ttu-id="9b5ef-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="9b5ef-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="9b5ef-107">備註</span><span class="sxs-lookup"><span data-stu-id="9b5ef-107">Remarks</span></span>

<span data-ttu-id="9b5ef-108">使用 [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) 介面寫入具有指定格式的中繼資料 blob，並使用 [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) 介面進行讀取。</span><span class="sxs-lookup"><span data-stu-id="9b5ef-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="9b5ef-109">中繼資料 blob 對媒體基礎管線和元件而言是不透明的。</span><span class="sxs-lookup"><span data-stu-id="9b5ef-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="9b5ef-110">屬性會套用至空間音訊媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9b5ef-110">The attribute is applied to the spatial audio media type.</span></span> <span data-ttu-id="9b5ef-111">如果下游元件不支援 GUID 指定的元資料格式，則元件應該拒絕輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9b5ef-111">If a downstream component does not support the metadata format specified by the GUID, the component should reject the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b5ef-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b5ef-112">Requirements</span></span>



| <span data-ttu-id="9b5ef-113">需求</span><span class="sxs-lookup"><span data-stu-id="9b5ef-113">Requirement</span></span> | <span data-ttu-id="9b5ef-114">值</span><span class="sxs-lookup"><span data-stu-id="9b5ef-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5ef-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b5ef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9b5ef-116">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b5ef-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9b5ef-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b5ef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9b5ef-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="9b5ef-118">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9b5ef-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9b5ef-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b5ef-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b5ef-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
