---
description: 指定編碼器是否執行反向電視電影。
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: 'AVEncVideoInverseTelecineEnable 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109497"
---
# <a name="avencvideoinversetelecineenable-property"></a><span data-ttu-id="6d07d-103">AVEncVideoInverseTelecineEnable 屬性</span><span class="sxs-lookup"><span data-stu-id="6d07d-103">AVEncVideoInverseTelecineEnable property</span></span>

<span data-ttu-id="6d07d-104">指定編碼器是否執行反向電視電影。</span><span class="sxs-lookup"><span data-stu-id="6d07d-104">Specifies whether the encoder performs inverse telecine.</span></span>

<span data-ttu-id="6d07d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6d07d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6d07d-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="6d07d-106">Data type</span></span>

<span data-ttu-id="6d07d-107">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="6d07d-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6d07d-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="6d07d-108">Property GUID</span></span>

<span data-ttu-id="6d07d-109">**CODECAPI \_ AVEncVideoInverseTelecineEnable**</span><span class="sxs-lookup"><span data-stu-id="6d07d-109">**CODECAPI\_AVEncVideoInverseTelecineEnable**</span></span>

## <a name="remarks"></a><span data-ttu-id="6d07d-110">備註</span><span class="sxs-lookup"><span data-stu-id="6d07d-110">Remarks</span></span>

<span data-ttu-id="6d07d-111">如果值為 **VARIANT \_ TRUE**，編碼器會執行反向電視電影。</span><span class="sxs-lookup"><span data-stu-id="6d07d-111">If the value is **VARIANT\_TRUE**, the encoder performs inverse telecine.</span></span> <span data-ttu-id="6d07d-112">如果不需要反向電視電影，請將此屬性設定為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6d07d-112">If inverse telecine is not required, set this property to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="6d07d-113">若要在編碼器之外執行反向電視，請將此屬性設定為 **VARIANT \_ FALSE** ，並將 [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) 屬性設定為 eAVEncVideoOutputScan \_ SameAsInput。</span><span class="sxs-lookup"><span data-stu-id="6d07d-113">To perform inverse telecine outside of the encoder, set this property to **VARIANT\_FALSE** and set the [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) property to eAVEncVideoOutputScan\_SameAsInput.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d07d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d07d-114">Requirements</span></span>



| <span data-ttu-id="6d07d-115">需求</span><span class="sxs-lookup"><span data-stu-id="6d07d-115">Requirement</span></span> | <span data-ttu-id="6d07d-116">值</span><span class="sxs-lookup"><span data-stu-id="6d07d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d07d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d07d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d07d-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d07d-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6d07d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d07d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d07d-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d07d-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6d07d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6d07d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d07d-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d07d-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d07d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d07d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d07d-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="6d07d-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6d07d-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="6d07d-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




