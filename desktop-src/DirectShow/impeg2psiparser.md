---
description: 此介面的實作為使用 DirectShow SDK 的範例程式碼來提供。
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: IMpeg2PsiParser 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970494"
---
# <a name="impeg2psiparser-interface"></a><span data-ttu-id="cf29a-103">IMpeg2PsiParser 介面</span><span class="sxs-lookup"><span data-stu-id="cf29a-103">IMpeg2PsiParser interface</span></span>

<span data-ttu-id="cf29a-104">此介面的實作為使用 DirectShow SDK 的範例程式碼來提供。</span><span class="sxs-lookup"><span data-stu-id="cf29a-104">The implementation of this interface is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="cf29a-105">這不是支援的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="cf29a-105">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="cf29a-106">此 `IMpeg2PsiParser` 介面會從 psi 剖析器篩選器中取出程式特定資訊 (psi) ，此篩選器會在 DIRECTSHOW SDK 中以範例篩選器的形式提供。</span><span class="sxs-lookup"><span data-stu-id="cf29a-106">The `IMpeg2PsiParser` interface retrieves Program Specific Information (PSI) from the PSI Parser filter, which is provided in the DirectShow SDK as a sample filter.</span></span> <span data-ttu-id="cf29a-107">應用程式可以使用此篩選器，將程式識別碼對應至 MPEG-2 信號篩選器上的 (Pid) 。</span><span class="sxs-lookup"><span data-stu-id="cf29a-107">An application can use this filter to map program IDs (PIDs) on the MPEG-2 Demultiplexer filter.</span></span>

## <a name="members"></a><span data-ttu-id="cf29a-108">成員</span><span class="sxs-lookup"><span data-stu-id="cf29a-108">Members</span></span>

<span data-ttu-id="cf29a-109">**IMpeg2PsiParser** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="cf29a-109">The **IMpeg2PsiParser** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cf29a-110">**IMpeg2PsiParser** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cf29a-110">**IMpeg2PsiParser** also has these types of members:</span></span>

-   [<span data-ttu-id="cf29a-111">方法</span><span class="sxs-lookup"><span data-stu-id="cf29a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cf29a-112">方法</span><span class="sxs-lookup"><span data-stu-id="cf29a-112">Methods</span></span>

<span data-ttu-id="cf29a-113">**IMpeg2PsiParser** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cf29a-113">The **IMpeg2PsiParser** interface has these methods.</span></span>



| <span data-ttu-id="cf29a-114">方法</span><span class="sxs-lookup"><span data-stu-id="cf29a-114">Method</span></span>                                                                             | <span data-ttu-id="cf29a-115">描述</span><span class="sxs-lookup"><span data-stu-id="cf29a-115">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf29a-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf29a-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span></span>         | <span data-ttu-id="cf29a-117">根據程式編號，找出程式的對應表 (PMT) PID。</span><span class="sxs-lookup"><span data-stu-id="cf29a-117">Finds the Program Map Table (PMT) PID for a program, given the program number.</span></span><br/> |
| [<span data-ttu-id="cf29a-118">**GetCountOfElementaryStreams**</span><span class="sxs-lookup"><span data-stu-id="cf29a-118">**GetCountOfElementaryStreams**</span></span>](impeg2psiparser-getcountofelementarystreams.md) | <span data-ttu-id="cf29a-119">抓取指定程式中的基本資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="cf29a-119">Retrieves the number of elementary streams in a specified program.</span></span><br/>             |
| [<span data-ttu-id="cf29a-120">**GetCountOfPrograms**</span><span class="sxs-lookup"><span data-stu-id="cf29a-120">**GetCountOfPrograms**</span></span>](impeg2psiparser-getcountofprograms.md)                   | <span data-ttu-id="cf29a-121">捕獲傳輸資料流程中的程式數目。</span><span class="sxs-lookup"><span data-stu-id="cf29a-121">Retrieves the number of programs in the transport stream.</span></span><br/>                      |
| [<span data-ttu-id="cf29a-122">**GetPatVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="cf29a-122">**GetPatVersionNumber**</span></span>](impeg2psiparser-getpatversionnumber.md)                 | <span data-ttu-id="cf29a-123">\_從程式關聯資料表中，抓取 (PAT) 的 [版本號碼] 欄位。</span><span class="sxs-lookup"><span data-stu-id="cf29a-123">Retrieves the version\_number field from the Program Association Table (PAT).</span></span><br/>  |
| [<span data-ttu-id="cf29a-124">**GetPmtVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="cf29a-124">**GetPmtVersionNumber**</span></span>](impeg2psiparser-getpmtversionnumber.md)                 | <span data-ttu-id="cf29a-125">\_從指定的 PMT 抓取版本號碼欄位。</span><span class="sxs-lookup"><span data-stu-id="cf29a-125">Retrieves the version\_number field from a specified PMT.</span></span><br/>                      |
| <span data-ttu-id="cf29a-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf29a-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span></span>           | <span data-ttu-id="cf29a-127">抓取程式中指定之基本資料流程的 PID 指派。</span><span class="sxs-lookup"><span data-stu-id="cf29a-127">Retrieves the PID assignment for a specified elementary stream in a program.</span></span><br/>   |
| <span data-ttu-id="cf29a-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf29a-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span></span>           | <span data-ttu-id="cf29a-129">抓取指定之 PMT 的 PID 指派。</span><span class="sxs-lookup"><span data-stu-id="cf29a-129">Retrieves the PID assignment for a specified PMT.</span></span><br/>                              |
| [<span data-ttu-id="cf29a-130">**GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="cf29a-130">**GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)           | <span data-ttu-id="cf29a-131">抓取指定程式的程式編號。</span><span class="sxs-lookup"><span data-stu-id="cf29a-131">Retrieves the program number for a specified program.</span></span><br/>                          |
| <span data-ttu-id="cf29a-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf29a-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span></span>                 | <span data-ttu-id="cf29a-133">抓取程式中指定之基本資料流程的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="cf29a-133">Retrieves the stream type for a specified elementary stream in a program.</span></span><br/>      |
| [<span data-ttu-id="cf29a-134">**GetTransportStreamId**</span><span class="sxs-lookup"><span data-stu-id="cf29a-134">**GetTransportStreamId**</span></span>](impeg2psiparser-gettransportstreamid.md)               | <span data-ttu-id="cf29a-135">\_從 PAT 抓取傳輸資料流程 \_ 識別碼欄位。</span><span class="sxs-lookup"><span data-stu-id="cf29a-135">Retrieves the transport\_stream\_id field from the PAT.</span></span><br/>                        |



 

## <a name="see-also"></a><span data-ttu-id="cf29a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf29a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf29a-137">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="cf29a-137">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 
