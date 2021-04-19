---
description: 指定音訊端點 simulataneously 可轉譯的動態音訊物件最大數目。
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: 'MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977949"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a><span data-ttu-id="8fee8-103">MF \_ MT \_ 空間 \_ 音訊 \_ 最大 \_ 動態 \_ 物件屬性</span><span class="sxs-lookup"><span data-stu-id="8fee8-103">MF\_MT\_SPATIAL\_AUDIO\_MAX\_DYNAMIC\_OBJECTS attribute</span></span>

<span data-ttu-id="8fee8-104">指定音訊端點 simulataneously 可轉譯的動態音訊物件最大數目。</span><span class="sxs-lookup"><span data-stu-id="8fee8-104">Specifies the maximum number of dynamic audio objects that can be rendered by the audio endpoint simulataneously.</span></span>

## <a name="data-type"></a><span data-ttu-id="8fee8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8fee8-105">Data type</span></span>

<span data-ttu-id="8fee8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8fee8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8fee8-107">備註</span><span class="sxs-lookup"><span data-stu-id="8fee8-107">Remarks</span></span>

<span data-ttu-id="8fee8-108">[**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample)可能包含的樣本數比這個屬性所指定的數目少。</span><span class="sxs-lookup"><span data-stu-id="8fee8-108">An [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) may contain fewer samples than the number specified by this attribute.</span></span> <span data-ttu-id="8fee8-109">如果範例包含的音訊物件數目超過這個屬性所指定的數目，則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8fee8-109">If a sample contains more audio objects than specified by this attribute, the behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fee8-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fee8-110">Requirements</span></span>



| <span data-ttu-id="8fee8-111">需求</span><span class="sxs-lookup"><span data-stu-id="8fee8-111">Requirement</span></span> | <span data-ttu-id="8fee8-112">值</span><span class="sxs-lookup"><span data-stu-id="8fee8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fee8-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fee8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8fee8-114">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fee8-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8fee8-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fee8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8fee8-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="8fee8-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8fee8-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8fee8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fee8-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fee8-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




