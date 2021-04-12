---
description: 取得遠端引擎的端點位址。
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPeerToPeerEngine：： GetPlaybackEndpoint 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6ee25dbd456086227e88fcb8bf7708a39e26eb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509947"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span data-ttu-id="969c6-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine：： GetPlaybackEndpoint 方法</span><span class="sxs-lookup"><span data-stu-id="969c6-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint method</span></span>

<span data-ttu-id="969c6-104">取得遠端引擎的端點位址。</span><span class="sxs-lookup"><span data-stu-id="969c6-104">Gets the endpoint address of a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="969c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="969c6-105">Syntax</span></span>


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="969c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="969c6-106">Parameters</span></span>

<span data-ttu-id="969c6-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="969c6-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="969c6-108">如果遠端引擎使用驗證，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="969c6-108">true if the remote engine uses authentication; otherwise, false.</span></span>

<span data-ttu-id="969c6-109">*pEndpoint* </span><span class="sxs-lookup"><span data-stu-id="969c6-109">*pEndpoint* </span></span>  
<span data-ttu-id="969c6-110">傳回時，包含遠端播放電腦之端點位址的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="969c6-110">On return, a COM string containing the endpoint address of the remote playback machine.</span></span>

<span data-ttu-id="969c6-111">*Setsessionkey* </span><span class="sxs-lookup"><span data-stu-id="969c6-111">*sessionKey* </span></span>  
<span data-ttu-id="969c6-112">傳回時，包含用於加密之工作階段金鑰的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="969c6-112">On return, a COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="969c6-113">*pRemoteVersion* </span><span class="sxs-lookup"><span data-stu-id="969c6-113">*pRemoteVersion* </span></span>  
<span data-ttu-id="969c6-114">傳回時為遠端引擎的版本。</span><span class="sxs-lookup"><span data-stu-id="969c6-114">On return, the version of the remote engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="969c6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="969c6-115">Return value</span></span>

<span data-ttu-id="969c6-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="969c6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="969c6-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="969c6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="969c6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="969c6-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="969c6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="969c6-119">Header</span></span></p></td><td><span data-ttu-id="969c6-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="969c6-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="969c6-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="969c6-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="969c6-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="969c6-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
