---
description: 設定指定之圖形記錄檔的目前播放電腦。
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine2：： SetPlaybackMachine 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d7366da4aa999828309136900edfe725af4f622
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510340"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span data-ttu-id="9e506-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2：： SetPlaybackMachine 方法</span><span class="sxs-lookup"><span data-stu-id="9e506-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2::SetPlaybackMachine method</span></span>

<span data-ttu-id="9e506-104">設定指定之圖形記錄檔的目前播放電腦。</span><span class="sxs-lookup"><span data-stu-id="9e506-104">Sets the current playback machine for the specified graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e506-105">語法</span><span class="sxs-lookup"><span data-stu-id="9e506-105">Syntax</span></span>


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a><span data-ttu-id="9e506-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e506-106">Parameters</span></span>

<span data-ttu-id="9e506-107">*記錄檔* </span><span class="sxs-lookup"><span data-stu-id="9e506-107">*logFile* </span></span>  
<span data-ttu-id="9e506-108">寫入圖形記錄檔名稱的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="9e506-108">A COM string contianing the name of the graphics log.</span></span>

<span data-ttu-id="9e506-109">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="9e506-109">*bUseAuthentication* </span></span>  
<span data-ttu-id="9e506-110">true 表示使用驗證;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="9e506-110">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="9e506-111">*機* </span><span class="sxs-lookup"><span data-stu-id="9e506-111">*machine* </span></span>  
<span data-ttu-id="9e506-112">包含播放電腦名稱稱的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="9e506-112">A COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e506-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e506-113">Return value</span></span>

<span data-ttu-id="9e506-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9e506-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e506-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9e506-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e506-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e506-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9e506-117">標頭</span><span class="sxs-lookup"><span data-stu-id="9e506-117">Header</span></span></p></td><td><span data-ttu-id="9e506-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9e506-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9e506-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e506-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9e506-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="9e506-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
