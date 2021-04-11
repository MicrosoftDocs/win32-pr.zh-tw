---
description: 多媒體串流物件
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: 多媒體串流物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321651"
---
# <a name="multimedia-streaming-objects"></a><span data-ttu-id="a24fa-103">多媒體串流物件</span><span class="sxs-lookup"><span data-stu-id="a24fa-103">Multimedia Streaming Objects</span></span>

> [!Note]  
> <span data-ttu-id="a24fa-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="a24fa-104">This API is deprecated.</span></span> <span data-ttu-id="a24fa-105">新的應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="a24fa-105">New applications should not use it.</span></span>

 

<span data-ttu-id="a24fa-106">下表描述多媒體串流物件。</span><span class="sxs-lookup"><span data-stu-id="a24fa-106">The following table describes the multimedia streaming objects.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a24fa-107">CLSID</span><span class="sxs-lookup"><span data-stu-id="a24fa-107">CLSID</span></span></th>
<th><span data-ttu-id="a24fa-108">Description</span><span class="sxs-lookup"><span data-stu-id="a24fa-108">Description</span></span></th>
<th><span data-ttu-id="a24fa-109">支援的介面</span><span class="sxs-lookup"><span data-stu-id="a24fa-109">Interfaces supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a24fa-110">CLSID_AMMediaTypeStream</span><span class="sxs-lookup"><span data-stu-id="a24fa-110">CLSID_AMMediaTypeStream</span></span></td>
<td><span data-ttu-id="a24fa-111">可以為任何支援 DirectShow 的資料類型建立媒體範例</span><span class="sxs-lookup"><span data-stu-id="a24fa-111">Can create media samples for any DirectShow-supported data type</span></span></td>
<td><ul>
<li><span data-ttu-id="a24fa-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-112"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-113"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-114"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a24fa-116">CLSID_AMAudioData</span><span class="sxs-lookup"><span data-stu-id="a24fa-116">CLSID_AMAudioData</span></span></td>
<td><span data-ttu-id="a24fa-117"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a>音訊容器物件的執行。</span><span class="sxs-lookup"><span data-stu-id="a24fa-117">Implementation of <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> audio container object.</span></span></td>
<td><ul>
<li><span data-ttu-id="a24fa-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-118"><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a24fa-119">CLSID_AMDirectDrawStream</span><span class="sxs-lookup"><span data-stu-id="a24fa-119">CLSID_AMDirectDrawStream</span></span></td>
<td><span data-ttu-id="a24fa-120">可以新增至 DirectShow 多媒體串流的 DirectDraw 媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="a24fa-120">DirectDraw media stream that can be added to a DirectShow multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="a24fa-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-121"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-122"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-123"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-124"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-125"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a24fa-126">CLSID_AMMultiMediaStream</span><span class="sxs-lookup"><span data-stu-id="a24fa-126">CLSID_AMMultiMediaStream</span></span></td>
<td><span data-ttu-id="a24fa-127">多媒體串流的 DirectShow 實行。</span><span class="sxs-lookup"><span data-stu-id="a24fa-127">DirectShow implementation of multimedia stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="a24fa-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-128"><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-129"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a24fa-130">CLSID_MediaStreamFilter</span><span class="sxs-lookup"><span data-stu-id="a24fa-130">CLSID_MediaStreamFilter</span></span></td>
<td><span data-ttu-id="a24fa-131">透過 <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> 介面提供 CLSID_AMMultiMediaStream 物件的多媒體串流處理功能。</span><span class="sxs-lookup"><span data-stu-id="a24fa-131">Provides multimedia streaming functionality for the CLSID_AMMultiMediaStream object through the <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> interface.</span></span></td>
<td><ul>
<li><span data-ttu-id="a24fa-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a24fa-133">N/A</span><span class="sxs-lookup"><span data-stu-id="a24fa-133">N/A</span></span></td>
<td><span data-ttu-id="a24fa-134">CLSID_AMMediaTypeStream 物件所建立的範例。</span><span class="sxs-lookup"><span data-stu-id="a24fa-134">Samples created by the CLSID_AMMediaTypeStream object.</span></span></td>
<td><ul>
<li><span data-ttu-id="a24fa-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-135"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-136"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-137"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a24fa-138">N/A</span><span class="sxs-lookup"><span data-stu-id="a24fa-138">N/A</span></span></td>
<td><span data-ttu-id="a24fa-139">DirectDraw 資料流程所建立的範例。</span><span class="sxs-lookup"><span data-stu-id="a24fa-139">Samples created by the DirectDraw stream.</span></span></td>
<td><ul>
<li><span data-ttu-id="a24fa-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-140"><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-141"><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></span></span></li>
<li><span data-ttu-id="a24fa-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="a24fa-142"><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



