---
description: 設定影片解碼所使用的背景工作執行緒數目。
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: 'CODECAPI_AVDecNumWorkerThreads 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973405"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a><span data-ttu-id="ca820-103">CODECAPI \_ AVDecNumWorkerThreads 屬性</span><span class="sxs-lookup"><span data-stu-id="ca820-103">CODECAPI\_AVDecNumWorkerThreads property</span></span>

<span data-ttu-id="ca820-104">設定影片解碼所使用的背景工作執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="ca820-104">Sets the number of worker threads that are used by a video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="ca820-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ca820-105">Data type</span></span>

<span data-ttu-id="ca820-106">**LONG** (**VT \_ I4**) </span><span class="sxs-lookup"><span data-stu-id="ca820-106">**LONG** (**VT\_I4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ca820-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="ca820-107">Property GUID</span></span>

<span data-ttu-id="ca820-108">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="ca820-108">CODECAPI\_AVDecNumWorkerThreads</span></span>

## <a name="remarks"></a><span data-ttu-id="ca820-109">備註</span><span class="sxs-lookup"><span data-stu-id="ca820-109">Remarks</span></span>

<span data-ttu-id="ca820-110">如果值為1，則此解碼器會選取執行緒的數目。</span><span class="sxs-lookup"><span data-stu-id="ca820-110">If the value is  1, the decoder selects the number of threads.</span></span>

<span data-ttu-id="ca820-111">針對 [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) 介面，將此屬性設定為 **LONG** 值， (**VT \_ I4**) 。</span><span class="sxs-lookup"><span data-stu-id="ca820-111">For the [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) interface, set this property as a **LONG** value (**VT\_I4**).</span></span> <span data-ttu-id="ca820-112">針對 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，將此屬性設定為 **UINT32**，雖然值已簽署。</span><span class="sxs-lookup"><span data-stu-id="ca820-112">For the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, set this property as a **UINT32**, although the value is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca820-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca820-113">Requirements</span></span>



| <span data-ttu-id="ca820-114">需求</span><span class="sxs-lookup"><span data-stu-id="ca820-114">Requirement</span></span> | <span data-ttu-id="ca820-115">值</span><span class="sxs-lookup"><span data-stu-id="ca820-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca820-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca820-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ca820-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca820-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="ca820-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca820-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ca820-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca820-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ca820-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ca820-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca820-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca820-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca820-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca820-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca820-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ca820-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ca820-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ca820-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

