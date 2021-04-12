---
description: 回呼函數，用來在捕捉或播放期間通知主機錯誤。
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFileIOCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109248"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span data-ttu-id="a1ba4-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="a1ba4-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback::ResultCallback method</span></span>

<span data-ttu-id="a1ba4-104">回呼函數，用來在捕捉或播放期間通知主機錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1ba4-104">A callback function used to notify the host of errors while during capture or playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ba4-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1ba4-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a><span data-ttu-id="a1ba4-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1ba4-106">Parameters</span></span>

<span data-ttu-id="a1ba4-107">*resultState* </span><span class="sxs-lookup"><span data-stu-id="a1ba4-107">*resultState* </span></span>  
<span data-ttu-id="a1ba4-108">指出所遇到的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="a1ba4-108">Indicates the kind of error encountered.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1ba4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1ba4-109">Return value</span></span>

<span data-ttu-id="a1ba4-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a1ba4-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1ba4-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a1ba4-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1ba4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1ba4-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a1ba4-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a1ba4-113">Header</span></span></p></td><td><span data-ttu-id="a1ba4-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a1ba4-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a1ba4-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1ba4-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a1ba4-116">**IFileIOCallback**</span><span class="sxs-lookup"><span data-stu-id="a1ba4-116">**IFileIOCallback**</span></span>](/windows/desktop/direct3dtools/ifileiocallback)

 

 
