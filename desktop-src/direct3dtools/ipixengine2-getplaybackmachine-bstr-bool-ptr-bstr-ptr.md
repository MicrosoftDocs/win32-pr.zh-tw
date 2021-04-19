---
description: 取得目前播放電腦的相關資訊。
MS-HAID: vspixengine.IPixEngine2\_GetPlaybackMachine\_BSTR\_BOOL\_ptr\_BSTR\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2：： GetPlaybackMachine 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D6C3C391-F039-4A5A-AA88-87A3624ECAD2
api_name:
- IPixEngine2.GetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c572d1a87fb537fd53a7f3e8f8048d1046980b20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972121"
---
# <a name="span-idvspixengineipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptrspanipixengine2getplaybackmachine-method"></a><span data-ttu-id="64267-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2：： GetPlaybackMachine 方法</span><span class="sxs-lookup"><span data-stu-id="64267-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2::GetPlaybackMachine method</span></span>

<span data-ttu-id="64267-104">取得目前播放電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="64267-104">Gets information about the current playback machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="64267-105">語法</span><span class="sxs-lookup"><span data-stu-id="64267-105">Syntax</span></span>


```C++
HRESULT GetPlaybackMachine(
   BSTR   logFile,
   BOOL * pUseAuthentication,
   BSTR * pMachine
);
```

## <a name="parameters"></a><span data-ttu-id="64267-106">參數</span><span class="sxs-lookup"><span data-stu-id="64267-106">Parameters</span></span>

<span data-ttu-id="64267-107">*記錄檔* </span><span class="sxs-lookup"><span data-stu-id="64267-107">*logFile* </span></span>  
<span data-ttu-id="64267-108">COM 字串，其中包含相關聯圖形記錄檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="64267-108">A COM string containing the name of the associated graphics log.</span></span>

<span data-ttu-id="64267-109">*pUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="64267-109">*pUseAuthentication* </span></span>  
<span data-ttu-id="64267-110">傳回時，如果連接使用驗證，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="64267-110">On return, true if the connection uses authentication; otherwise, false.</span></span>

<span data-ttu-id="64267-111">*pMachine* </span><span class="sxs-lookup"><span data-stu-id="64267-111">*pMachine* </span></span>  
<span data-ttu-id="64267-112">傳回時，包含播放電腦名稱稱的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="64267-112">On return, a COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="64267-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="64267-113">Return value</span></span>

<span data-ttu-id="64267-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="64267-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64267-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="64267-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="64267-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="64267-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="64267-117">標頭</span><span class="sxs-lookup"><span data-stu-id="64267-117">Header</span></span></p></td><td><span data-ttu-id="64267-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="64267-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="64267-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="64267-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="64267-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="64267-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
