---
description: 下列 Guid 會定義 Advanced 系統格式的相互排除物件 (ASF) 資料流程的類型。
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: 'ASF 相互排除類型 Guid (Wmcontainer .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191089"
---
# <a name="asf-mutual-exclusion-type-guids"></a><span data-ttu-id="6a98f-103">ASF 相互排除類型 Guid</span><span class="sxs-lookup"><span data-stu-id="6a98f-103">ASF Mutual Exclusion Type GUIDs</span></span>

<span data-ttu-id="6a98f-104">下列 Guid 會定義 Advanced 系統格式的相互排除物件 (ASF) 資料流程的類型。</span><span class="sxs-lookup"><span data-stu-id="6a98f-104">The following GUIDs define the types for the mutual exclusion object for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="6a98f-105">常數</span><span class="sxs-lookup"><span data-stu-id="6a98f-105">Constant</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="6a98f-106">描述</span><span class="sxs-lookup"><span data-stu-id="6a98f-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <span data-ttu-id="6a98f-107"><dt>**MFASFMutexType \_ 語言**</dt></span><span class="sxs-lookup"><span data-stu-id="6a98f-107"><dt>**MFASFMutexType\_Language**</dt></span></span> </dl>                 | <span data-ttu-id="6a98f-108">資料流程是依語言相互排斥。</span><span class="sxs-lookup"><span data-stu-id="6a98f-108">The streams are mutually exclusive by language.</span></span> <span data-ttu-id="6a98f-109">這種相互排除類型類似于 DVD 上的音訊曲目。</span><span class="sxs-lookup"><span data-stu-id="6a98f-109">This type of mutual exclusion is similar to the audio tracks on a DVD.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <span data-ttu-id="6a98f-110"><dt>**MFASFMutexType \_ 位元速率**</dt></span><span class="sxs-lookup"><span data-stu-id="6a98f-110"><dt>**MFASFMutexType\_Bitrate**</dt></span></span> </dl>                     | <span data-ttu-id="6a98f-111">資料流程會以位元速率互斥。</span><span class="sxs-lookup"><span data-stu-id="6a98f-111">The streams are mutually exclusive by bit rate.</span></span> <span data-ttu-id="6a98f-112">這種相互排除也稱為「多位元率」（ (MBR) 排除）。</span><span class="sxs-lookup"><span data-stu-id="6a98f-112">This type of mutual exclusion is also called multiple bit rate (MBR) exclusion.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <span data-ttu-id="6a98f-113"><dt>**MFASFMutexType \_ 簡報**</dt></span><span class="sxs-lookup"><span data-stu-id="6a98f-113"><dt>**MFASFMutexType\_Presentation**</dt></span></span> </dl> | <span data-ttu-id="6a98f-114">這些資料流程在簡報時是互斥的。</span><span class="sxs-lookup"><span data-stu-id="6a98f-114">The streams are mutually exclusive by presentation.</span></span> <span data-ttu-id="6a98f-115">這種類型可以用於許多案例，但應該只在內容相同但採用不同的表單時使用。</span><span class="sxs-lookup"><span data-stu-id="6a98f-115">This type can be used for many scenarios, but it should only be used when the content is the same but takes a different form.</span></span> <span data-ttu-id="6a98f-116">例如，兩個包含相同影片的串流，其中一個格式化為填滿螢幕，另一個則維持原始寬螢幕外觀比例，則應該使用此類型來互斥。</span><span class="sxs-lookup"><span data-stu-id="6a98f-116">For example, two streams containing the same video, one formatted to fill the screen and the other maintaining the original widescreen aspect ratio, should be made mutually exclusive by using this type.</span></span> <span data-ttu-id="6a98f-117">另一個範例是包含不同角度之相同場景拍攝影片的串流。</span><span class="sxs-lookup"><span data-stu-id="6a98f-117">Another example is streams containing video of the same scene shot from different angles.</span></span><br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <span data-ttu-id="6a98f-118"><dt>**MFASFMutexType \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="6a98f-118"><dt>**MFASFMutexType\_Unknown**</dt></span></span> </dl>                     | <span data-ttu-id="6a98f-119">資料流程會根據自訂準則相互排斥。</span><span class="sxs-lookup"><span data-stu-id="6a98f-119">The streams are mutually exclusive based on custom criteria.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="6a98f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a98f-120">Requirements</span></span>



| <span data-ttu-id="6a98f-121">需求</span><span class="sxs-lookup"><span data-stu-id="6a98f-121">Requirement</span></span> | <span data-ttu-id="6a98f-122">值</span><span class="sxs-lookup"><span data-stu-id="6a98f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a98f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a98f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6a98f-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a98f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6a98f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a98f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6a98f-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a98f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a98f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6a98f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a98f-128"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a98f-128"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a98f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a98f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a98f-130">**IMFASFMutualExclusion：： GetType**</span><span class="sxs-lookup"><span data-stu-id="6a98f-130">**IMFASFMutualExclusion::GetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[<span data-ttu-id="6a98f-131">**IMFASFMutualExclusion：： >advanced.field.settype**</span><span class="sxs-lookup"><span data-stu-id="6a98f-131">**IMFASFMutualExclusion::SetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[<span data-ttu-id="6a98f-132">媒體基礎常數</span><span class="sxs-lookup"><span data-stu-id="6a98f-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




