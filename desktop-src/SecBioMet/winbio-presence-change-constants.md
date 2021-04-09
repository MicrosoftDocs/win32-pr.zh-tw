---
title: 'WINBIO_PRESENCE_CHANGE 常數 (Winbio \_ 類型 .h) '
description: 描述當 Windows 生物特徵辨識架構監視個人是否存在時可能發生的變更類型。
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024696"
---
# <a name="winbio_presence_change-constants"></a><span data-ttu-id="52d27-103">WINBIO \_ 狀態 \_ 變更常數</span><span class="sxs-lookup"><span data-stu-id="52d27-103">WINBIO\_PRESENCE\_CHANGE Constants</span></span>

<span data-ttu-id="52d27-104">描述當 Windows 生物特徵辨識架構監視個人是否存在時可能發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="52d27-104">Describes the types of changes that can occur when the Windows Biometric Framework monitors the presence of individuals.</span></span>



| <span data-ttu-id="52d27-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="52d27-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="52d27-106">Description</span><span class="sxs-lookup"><span data-stu-id="52d27-106">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <span data-ttu-id="52d27-107"><dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 未知**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52d27-107"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="52d27-108">事件的類型未知。</span><span class="sxs-lookup"><span data-stu-id="52d27-108">The type of event is unknown.</span></span> <span data-ttu-id="52d27-109">此值用於未初始化的結構。</span><span class="sxs-lookup"><span data-stu-id="52d27-109">This value is used for the uninitialized structure.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <span data-ttu-id="52d27-110"><dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ \_ 全部更新**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="52d27-110"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UPDATE\_ALL**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="52d27-111">提供相機框架中所有目前臉部的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="52d27-111">Provides information about all of the faces current in the camera frame.</span></span><br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <span data-ttu-id="52d27-112"><dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 抵達**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="52d27-112"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_ARRIVE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="52d27-113">新臉部進入相機框架。</span><span class="sxs-lookup"><span data-stu-id="52d27-113">A new face entered the camera frame.</span></span><br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <span data-ttu-id="52d27-114"><dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 辨識**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="52d27-114"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_RECOGNIZE**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="52d27-115">臉部與已註冊的使用者相符。</span><span class="sxs-lookup"><span data-stu-id="52d27-115">A face was matched to an enrolled user.</span></span><br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <span data-ttu-id="52d27-116"><dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_**</dt>為 <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="52d27-116"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_DEPART**</dt> <dt>4</dt></span></span> </dl>              | <span data-ttu-id="52d27-117">先前偵測到的臉部已離開相機框架一段時間。</span><span class="sxs-lookup"><span data-stu-id="52d27-117">A previously detected face has been out of the camera frame for a period of time.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <span data-ttu-id="52d27-118"><dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 追蹤**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="52d27-118"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_TRACK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="52d27-119">提供有關周框方塊的更新資訊，以及目前在相機框架中的臉部子集的拒絕詳細資料值。</span><span class="sxs-lookup"><span data-stu-id="52d27-119">Provides updates information about the bounding box and reject detail values for a subset of the faces that are currently in the camera frame.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52d27-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="52d27-120">Requirements</span></span>



| <span data-ttu-id="52d27-121">需求</span><span class="sxs-lookup"><span data-stu-id="52d27-121">Requirement</span></span> | <span data-ttu-id="52d27-122">值</span><span class="sxs-lookup"><span data-stu-id="52d27-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52d27-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52d27-123">Minimum supported client</span></span><br/> | <span data-ttu-id="52d27-124">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52d27-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="52d27-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52d27-125">Minimum supported server</span></span><br/> | <span data-ttu-id="52d27-126">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52d27-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="52d27-127">標頭</span><span class="sxs-lookup"><span data-stu-id="52d27-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d27-128"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="52d27-128"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





