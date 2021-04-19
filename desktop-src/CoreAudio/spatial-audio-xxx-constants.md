---
description: 空間 \_ 音訊 \_ XXX 常數會定義與空間音效功能相關的值。
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: 'SPATIAL_AUDIO_XXX 常數 (SpatialAudioMetadata) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001143"
---
# <a name="spatial_audio_xxx-constants"></a><span data-ttu-id="b0354-103">空間 \_ 音訊 \_ XXX 常數</span><span class="sxs-lookup"><span data-stu-id="b0354-103">SPATIAL\_AUDIO\_XXX Constants</span></span>

<span data-ttu-id="b0354-104">空間 \_ 音訊 \_ XXX 常數會定義與空間音效功能相關的值。</span><span class="sxs-lookup"><span data-stu-id="b0354-104">The SPATIAL\_AUDIO\_XXX constants define values related to spatial sound features.</span></span>



| <span data-ttu-id="b0354-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="b0354-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="b0354-106">Description</span><span class="sxs-lookup"><span data-stu-id="b0354-106">Description</span></span>                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <span data-ttu-id="b0354-107"><dt>**空間 \_音訊 \_ 位置**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="b0354-107"><dt>**SPATIAL\_AUDIO\_POSITION**</dt> <dt>200</dt></span></span> </dl>                                                   | <span data-ttu-id="b0354-108">標準的 Microsoft 定義空間音訊中繼資料命令，代表 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 所使用之標準模型中的接聽程式位置，其中接聽程式的標頭是座標處的位置， (0、0、0) （定義于計量區）。</span><span class="sxs-lookup"><span data-stu-id="b0354-108">A standard Microsoft-defined spatial audio metadata command which represents the listener position in the standard model used by [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) where the listener's head is position at coordinates (0,0,0), defined in meters.</span></span><br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <span data-ttu-id="b0354-109"><dt>**空間 \_音訊 \_ 位置 \_ 位元組 \_ 計數**</dt> <dt>sizeof (float) \* 3</dt></span><span class="sxs-lookup"><span data-stu-id="b0354-109"><dt>**SPATIAL\_AUDIO\_POSITION\_BYTE\_COUNT**</dt> <dt>sizeof(float) \* 3</dt></span></span> </dl> | <span data-ttu-id="b0354-110">指定 **空間 \_ 音訊 \_ 位置** 值的大小。</span><span class="sxs-lookup"><span data-stu-id="b0354-110">Specifies the size of the **SPATIAL\_AUDIO\_POSITION** value.</span></span><br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <span data-ttu-id="b0354-111"><dt>**空間 \_音訊 \_ 標準 \_ 命令 \_ 開始**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="b0354-111"><dt>**SPATIAL\_AUDIO\_STANDARD\_COMMANDS\_START**</dt> <dt>200</dt></span></span> </dl>    | <span data-ttu-id="b0354-112">指定 Microsoft 保留空間音訊中繼資料命令範圍的開始。</span><span class="sxs-lookup"><span data-stu-id="b0354-112">Specifies the start of the range of Microsoft-reserved spatial audio metadata commands.</span></span> <span data-ttu-id="b0354-113">自訂中繼資料命令僅限於命令識別碼 0-199。</span><span class="sxs-lookup"><span data-stu-id="b0354-113">Custom metadata commands are restricted to command IDs 0 - 199.</span></span> <span data-ttu-id="b0354-114">命令 200-255 已保留供 Microsoft 使用。</span><span class="sxs-lookup"><span data-stu-id="b0354-114">Commands 200 - 255 are reserved for Microsoft use.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="b0354-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0354-115">Requirements</span></span>



| <span data-ttu-id="b0354-116">需求</span><span class="sxs-lookup"><span data-stu-id="b0354-116">Requirement</span></span> | <span data-ttu-id="b0354-117">值</span><span class="sxs-lookup"><span data-stu-id="b0354-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0354-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b0354-118">Header</span></span><br/> | <dl> <span data-ttu-id="b0354-119"><dt>SpatialAudioMetadata。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0354-119"><dt>SpatialAudioMetadata.h</dt></span></span> </dl> |



 

 




