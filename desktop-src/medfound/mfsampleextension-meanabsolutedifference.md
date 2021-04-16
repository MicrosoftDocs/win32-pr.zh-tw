---
description: 這個屬性會傳回 Y 平面中所有宏區塊 (MAD) 的平均絕對差異。
ms.assetid: 7F0358F1-794A-4E75-8D97-3B91955E19EE
title: 'MFSampleExtension_MeanAbsoluteDifference 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4b7187b295071b8e27b68d9b5804aab6b2ddef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512613"
---
# <a name="mfsampleextension_meanabsolutedifference-attribute"></a><span data-ttu-id="32049-103">MFSampleExtension \_ MeanAbsoluteDifference 屬性</span><span class="sxs-lookup"><span data-stu-id="32049-103">MFSampleExtension\_MeanAbsoluteDifference attribute</span></span>

<span data-ttu-id="32049-104">這個屬性會傳回 Y 平面中所有宏區塊 (MAD) 的平均絕對差異。</span><span class="sxs-lookup"><span data-stu-id="32049-104">This attribute returns the mean absolute difference (MAD) across all macro-blocks in the Y plane.</span></span>

## <a name="data-type"></a><span data-ttu-id="32049-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="32049-105">Data type</span></span>

<span data-ttu-id="32049-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="32049-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="32049-107">備註</span><span class="sxs-lookup"><span data-stu-id="32049-107">Remarks</span></span>

<span data-ttu-id="32049-108">應用程式可以使用 [CODECAPI \_ AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)要求編碼器在輸出範例上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="32049-108">Application can request encoder to set this attribute on output samples by using [CODECAPI\_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32049-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="32049-109">Requirements</span></span>



| <span data-ttu-id="32049-110">需求</span><span class="sxs-lookup"><span data-stu-id="32049-110">Requirement</span></span> | <span data-ttu-id="32049-111">值</span><span class="sxs-lookup"><span data-stu-id="32049-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32049-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32049-112">Minimum supported client</span></span><br/> | <span data-ttu-id="32049-113">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32049-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="32049-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32049-114">Minimum supported server</span></span><br/> | <span data-ttu-id="32049-115">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32049-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="32049-116">標頭</span><span class="sxs-lookup"><span data-stu-id="32049-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="32049-117"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="32049-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32049-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32049-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32049-119">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="32049-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




