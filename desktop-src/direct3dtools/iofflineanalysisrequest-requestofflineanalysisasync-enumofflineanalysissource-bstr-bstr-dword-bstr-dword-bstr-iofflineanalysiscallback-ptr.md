---
description: 要求以指定的來源、資訊清單、參數和指定的框架執行離線分析。
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisRequest：： RequestOfflineAnalysisAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d027b9ec463c0bebfefca3ee7f9af4b50c514755
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385737"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span data-ttu-id="82bd1-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest：： RequestOfflineAnalysisAsync 方法</span><span class="sxs-lookup"><span data-stu-id="82bd1-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync method</span></span>

<span data-ttu-id="82bd1-104">要求以指定的來源、資訊清單、參數和指定的框架執行離線分析。</span><span class="sxs-lookup"><span data-stu-id="82bd1-104">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bd1-105">語法</span><span class="sxs-lookup"><span data-stu-id="82bd1-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="82bd1-106">參數</span><span class="sxs-lookup"><span data-stu-id="82bd1-106">Parameters</span></span>

<span data-ttu-id="82bd1-107">*analysisSource* </span><span class="sxs-lookup"><span data-stu-id="82bd1-107">*analysisSource* </span></span>  
<span data-ttu-id="82bd1-108">指定，其中分析來源來自快取的報表或播放。</span><span class="sxs-lookup"><span data-stu-id="82bd1-108">Specfies where the analysis source come from cached reports or from playback.</span></span>

<span data-ttu-id="82bd1-109">*manifestXml* </span><span class="sxs-lookup"><span data-stu-id="82bd1-109">*manifestXml* </span></span>  
<span data-ttu-id="82bd1-110">COM 字串，其中包含 XML 資訊清單檔的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="82bd1-110">A COM string containing the pathname of the XML manifest file.</span></span>

<span data-ttu-id="82bd1-111">*parametersXml* </span><span class="sxs-lookup"><span data-stu-id="82bd1-111">*parametersXml* </span></span>  
<span data-ttu-id="82bd1-112">COM 字串，其中包含 XML 參數檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="82bd1-112">A COM string containing the pathname of the XML parameters file.</span></span>

<span data-ttu-id="82bd1-113">*餅乾* </span><span class="sxs-lookup"><span data-stu-id="82bd1-113">*cookie* </span></span>  
<span data-ttu-id="82bd1-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="82bd1-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="82bd1-115">*captureFullFileName* </span><span class="sxs-lookup"><span data-stu-id="82bd1-115">*captureFullFileName* </span></span>  
<span data-ttu-id="82bd1-116">COM 字串，其中包含 capture 檔案的絕對路徑名稱 ( vsglog) 。</span><span class="sxs-lookup"><span data-stu-id="82bd1-116">A COM string containing the absolute pathname of the capture file (.vsglog).</span></span>

<span data-ttu-id="82bd1-117">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="82bd1-117">*frameNumber* </span></span>  
<span data-ttu-id="82bd1-118">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="82bd1-118">The specified frame.</span></span>

<span data-ttu-id="82bd1-119">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="82bd1-119">*outputFullFileName* </span></span>  
<span data-ttu-id="82bd1-120">COM 字串，其中包含寫入輸出之檔案的絕對路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="82bd1-120">A COM string containing the absolute pathname of the file where output is written.</span></span>

<span data-ttu-id="82bd1-121">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="82bd1-121">*requestCallback* </span></span>  
<span data-ttu-id="82bd1-122">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="82bd1-122">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="82bd1-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="82bd1-123">Return value</span></span>

<span data-ttu-id="82bd1-124">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="82bd1-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="82bd1-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="82bd1-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="82bd1-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="82bd1-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="82bd1-127">標頭</span><span class="sxs-lookup"><span data-stu-id="82bd1-127">Header</span></span></p></td><td><span data-ttu-id="82bd1-128">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="82bd1-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="82bd1-129"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="82bd1-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="82bd1-130">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="82bd1-130">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
