---
description: 以非同步方式設定用來連接到遠端引擎的端點位址。
MS-HAID: vspixengine.IPixEngine7\_SetPlaybackEndpointAsync\_BOOL\_BSTR\_BSTR\_RemotingVersion\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine7：： SetPlaybackEndpointAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4F76EFFF-F3CB-4BEA-999F-639876C7F792
api_name:
- IPixEngine7.SetPlaybackEndpointAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2e0970b1a2a786c828a24efef0ae9e4057dbe2cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688371"
---
# <a name="span-idvspixengineipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dwordspanipixengine7setplaybackendpointasync-method"></a><span data-ttu-id="b4c51-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7：： SetPlaybackEndpointAsync 方法</span><span class="sxs-lookup"><span data-stu-id="b4c51-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7::SetPlaybackEndpointAsync method</span></span>

<span data-ttu-id="b4c51-104">以非同步方式設定用來連接到遠端引擎的端點位址。</span><span class="sxs-lookup"><span data-stu-id="b4c51-104">Asynchronously sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c51-105">語法</span><span class="sxs-lookup"><span data-stu-id="b4c51-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpointAsync(
   BOOL              bUseAuthentication,
   BSTR              endpoint,
   BSTR              sessionKey,
   RemotingVersion   remoteVersion,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b4c51-106">參數</span><span class="sxs-lookup"><span data-stu-id="b4c51-106">Parameters</span></span>

<span data-ttu-id="b4c51-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="b4c51-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="b4c51-108">true 表示使用驗證;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="b4c51-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="b4c51-109">*端點* </span><span class="sxs-lookup"><span data-stu-id="b4c51-109">*endpoint* </span></span>  
<span data-ttu-id="b4c51-110">包含端點位址的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="b4c51-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="b4c51-111">*Setsessionkey* </span><span class="sxs-lookup"><span data-stu-id="b4c51-111">*sessionKey* </span></span>  
<span data-ttu-id="b4c51-112">COM 字串，其中包含用來加密的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="b4c51-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="b4c51-113">*remoteVersion* </span><span class="sxs-lookup"><span data-stu-id="b4c51-113">*remoteVersion* </span></span>  
<span data-ttu-id="b4c51-114">指定要使用的遠端引擎版本。</span><span class="sxs-lookup"><span data-stu-id="b4c51-114">Specifies the version of the remote engine to use.</span></span>

<span data-ttu-id="b4c51-115">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="b4c51-115">*versionCallback* </span></span>  
<span data-ttu-id="b4c51-116">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="b4c51-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b4c51-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b4c51-117">*requestCookie* </span></span>  
<span data-ttu-id="b4c51-118">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="b4c51-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b4c51-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b4c51-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b4c51-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="b4c51-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4c51-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4c51-121">Return value</span></span>

<span data-ttu-id="b4c51-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b4c51-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4c51-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b4c51-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c51-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4c51-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b4c51-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b4c51-125">Header</span></span></p></td><td><span data-ttu-id="b4c51-126">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b4c51-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b4c51-127"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4c51-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b4c51-128">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="b4c51-128">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
