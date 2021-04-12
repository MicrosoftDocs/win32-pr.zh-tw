---
description: 回呼函式，用來通知主機與呼叫堆疊相關聯之來源檔案的相關資訊。
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISourceFileInfoCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109861"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span data-ttu-id="fbb3d-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="fbb3d-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback method</span></span>

<span data-ttu-id="fbb3d-104">回呼函式，用來通知主機與呼叫堆疊相關聯之來源檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fbb3d-104">A callback function used to notify the host of information about source files associated with the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb3d-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbb3d-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="fbb3d-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbb3d-106">Parameters</span></span>

<span data-ttu-id="fbb3d-107">*計數* </span><span class="sxs-lookup"><span data-stu-id="fbb3d-107">*count* </span></span>  
<span data-ttu-id="fbb3d-108">傳回的原始程式檔數目。</span><span class="sxs-lookup"><span data-stu-id="fbb3d-108">The number of source files returned.</span></span>

<span data-ttu-id="fbb3d-109">*count0 \_ sourceFileInfoBuffer* </span><span class="sxs-lookup"><span data-stu-id="fbb3d-109">*count0\_sourceFileInfoBuffer* </span></span>  
<span data-ttu-id="fbb3d-110">來源檔案。</span><span class="sxs-lookup"><span data-stu-id="fbb3d-110">The source files.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbb3d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbb3d-111">Return value</span></span>

<span data-ttu-id="fbb3d-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fbb3d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbb3d-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fbb3d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb3d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbb3d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fbb3d-115">標頭</span><span class="sxs-lookup"><span data-stu-id="fbb3d-115">Header</span></span></p></td><td><span data-ttu-id="fbb3d-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fbb3d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fbb3d-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbb3d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fbb3d-118">**ISourceFileInfoCallback**</span><span class="sxs-lookup"><span data-stu-id="fbb3d-118">**ISourceFileInfoCallback**</span></span>](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
