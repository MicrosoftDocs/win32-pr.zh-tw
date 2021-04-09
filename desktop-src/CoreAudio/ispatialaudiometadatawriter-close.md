---
description: 完成元資料緩衝區所需的任何作業，並釋放指定的 ISpatialAudioMetadataItems 物件。
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: ISpatialAudioMetadataWriter：： Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111196"
---
# <a name="ispatialaudiometadatawriterclose-method"></a><span data-ttu-id="5374b-103">ISpatialAudioMetadataWriter：： Close 方法</span><span class="sxs-lookup"><span data-stu-id="5374b-103">ISpatialAudioMetadataWriter::Close method</span></span>

<span data-ttu-id="5374b-104">完成元資料緩衝區所需的任何作業，並釋放指定的 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) 物件。</span><span class="sxs-lookup"><span data-stu-id="5374b-104">Completes any needed operations on the metadata buffer and releases the specified [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5374b-105">語法</span><span class="sxs-lookup"><span data-stu-id="5374b-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="5374b-106">參數</span><span class="sxs-lookup"><span data-stu-id="5374b-106">Parameters</span></span>

<span data-ttu-id="5374b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5374b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5374b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5374b-108">Return value</span></span>

<span data-ttu-id="5374b-109">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5374b-109">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5374b-110">如果失敗，可能的傳回碼包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="5374b-110">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="5374b-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5374b-111">Return code</span></span>                                                                                                                     | <span data-ttu-id="5374b-112">Description</span><span class="sxs-lookup"><span data-stu-id="5374b-112">Description</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5374b-113"><dt>**SPTLAUD \_ MD \_ CONTOSO-CLNT \_ E \_ 未 \_ 開啟任何專案 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5374b-113"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_OPEN**</dt></span></span> </dl>            | <span data-ttu-id="5374b-114">未開啟具有 [**開啟**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open)之呼叫的已提供 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) 。</span><span class="sxs-lookup"><span data-stu-id="5374b-114">The supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) has not been opened with a call to [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span></span><br/> |
| <dl> <span data-ttu-id="5374b-115"><dt>**SPTLAUD \_ MD \_ CONTOSO-CLNT \_ E \_ 未 \_ 寫入任何專案 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5374b-115"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_WRITTEN**</dt></span></span> </dl>         | <span data-ttu-id="5374b-116">未將任何中繼資料專案寫入提供的 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)。</span><span class="sxs-lookup"><span data-stu-id="5374b-116">No metadata items have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                              |
| <dl> <span data-ttu-id="5374b-117"><dt>**SPTLAUD \_ MD \_ CONTOSO-CLNT \_ E \_ 專案 \_ 必須 \_ 有 \_ 命令**</dt></span><span class="sxs-lookup"><span data-stu-id="5374b-117"><dt>**SPTLAUD\_MD\_CLNT\_E\_ITEM\_MUST\_HAVE\_COMMANDS**</dt></span></span> </dl> | <span data-ttu-id="5374b-118">未將任何中繼資料命令寫入提供的 [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)。</span><span class="sxs-lookup"><span data-stu-id="5374b-118">No metadata commands have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                           |



 

## <a name="see-also"></a><span data-ttu-id="5374b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5374b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5374b-120">**ISpatialAudioMetadataWriter**</span><span class="sxs-lookup"><span data-stu-id="5374b-120">**ISpatialAudioMetadataWriter**</span></span>](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




