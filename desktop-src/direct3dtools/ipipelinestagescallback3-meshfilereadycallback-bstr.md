---
description: 回呼，會通知主機相關聯的要求所寫入的網格資訊。
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback3：： MeshFileReadyCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970499"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span data-ttu-id="a11a5-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3：： MeshFileReadyCallback 方法</span><span class="sxs-lookup"><span data-stu-id="a11a5-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback method</span></span>

<span data-ttu-id="a11a5-104">回呼，會通知主機相關聯的要求所寫入的網格資訊。</span><span class="sxs-lookup"><span data-stu-id="a11a5-104">A callback that notifies the host of Mesh information written by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a11a5-105">語法</span><span class="sxs-lookup"><span data-stu-id="a11a5-105">Syntax</span></span>


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a><span data-ttu-id="a11a5-106">參數</span><span class="sxs-lookup"><span data-stu-id="a11a5-106">Parameters</span></span>

<span data-ttu-id="a11a5-107">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="a11a5-107">*meshFilename* </span></span>  
<span data-ttu-id="a11a5-108">COM 字串，其中包含用來寫入網格資料之檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="a11a5-108">A COM string containing the pathname of the file where the mesh data is written.</span></span>

## <a name="return-value"></a><span data-ttu-id="a11a5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a11a5-109">Return value</span></span>

<span data-ttu-id="a11a5-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a11a5-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a11a5-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a11a5-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a11a5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a11a5-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a11a5-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a11a5-113">Header</span></span></p></td><td><span data-ttu-id="a11a5-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a11a5-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a11a5-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="a11a5-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a11a5-116">**IPipeLineStagesCallback3**</span><span class="sxs-lookup"><span data-stu-id="a11a5-116">**IPipeLineStagesCallback3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
