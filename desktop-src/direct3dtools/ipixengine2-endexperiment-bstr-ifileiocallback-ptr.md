---
description: 結束 experiement 並完成圖形記錄檔。
MS-HAID: vspixengine.IPixEngine2\_EndExperiment\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2：： EndExperiment 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0260F337-B279-4FE6-92F3-FCF70C2B8980
api_name:
- IPixEngine2.EndExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2638c75269f93e50fd1f9e4b6938b123cbd01e60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510046"
---
# <a name="span-idvspixengineipixengine2_endexperiment_bstr_ifileiocallback_ptrspanipixengine2endexperiment-method"></a><span data-ttu-id="d4255-103"><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>IPixEngine2：： EndExperiment 方法</span><span class="sxs-lookup"><span data-stu-id="d4255-103"><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>IPixEngine2::EndExperiment method</span></span>

<span data-ttu-id="d4255-104">結束 experiement 並完成圖形記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4255-104">Ends the experiement and completes the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4255-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4255-105">Syntax</span></span>


```C++
HRESULT EndExperiment(
   BSTR              logFile,
   IFileIOCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="d4255-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4255-106">Parameters</span></span>

<span data-ttu-id="d4255-107">*記錄檔* </span><span class="sxs-lookup"><span data-stu-id="d4255-107">*logFile* </span></span>  
<span data-ttu-id="d4255-108">COM 字串，包含圖形記錄檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4255-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="d4255-109">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="d4255-109">*pCallback* </span></span>  
<span data-ttu-id="d4255-110">回呼的位址，用來指出 experiement 已結束。</span><span class="sxs-lookup"><span data-stu-id="d4255-110">The address of a callback used to indicate that the experiement is ended.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4255-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4255-111">Return value</span></span>

<span data-ttu-id="d4255-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d4255-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4255-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d4255-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4255-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4255-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d4255-115">標頭</span><span class="sxs-lookup"><span data-stu-id="d4255-115">Header</span></span></p></td><td><span data-ttu-id="d4255-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="d4255-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d4255-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4255-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d4255-118">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="d4255-118">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
