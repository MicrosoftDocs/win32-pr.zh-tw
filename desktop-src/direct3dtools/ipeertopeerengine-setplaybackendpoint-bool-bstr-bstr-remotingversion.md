---
description: 設定用來連接到遠端引擎的端點位址。
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPeerToPeerEngine：： SetPlaybackEndpoint 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbec4826fb2659604a4b9f4388beed1829b42770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467863"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span data-ttu-id="9a3ca-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine：： SetPlaybackEndpoint 方法</span><span class="sxs-lookup"><span data-stu-id="9a3ca-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine::SetPlaybackEndpoint method</span></span>

<span data-ttu-id="9a3ca-104">設定用來連接到遠端引擎的端點位址。</span><span class="sxs-lookup"><span data-stu-id="9a3ca-104">Sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a3ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a3ca-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="9a3ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a3ca-106">Parameters</span></span>

<span data-ttu-id="9a3ca-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="9a3ca-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="9a3ca-108">true 表示使用驗證;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="9a3ca-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="9a3ca-109">*端點* </span><span class="sxs-lookup"><span data-stu-id="9a3ca-109">*endpoint* </span></span>  
<span data-ttu-id="9a3ca-110">包含端點位址的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="9a3ca-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="9a3ca-111">*Setsessionkey* </span><span class="sxs-lookup"><span data-stu-id="9a3ca-111">*sessionKey* </span></span>  
<span data-ttu-id="9a3ca-112">COM 字串，其中包含用來加密的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="9a3ca-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="9a3ca-113">*remoteVersion* </span><span class="sxs-lookup"><span data-stu-id="9a3ca-113">*remoteVersion* </span></span>  
<span data-ttu-id="9a3ca-114">指定要使用的遠端引擎版本。</span><span class="sxs-lookup"><span data-stu-id="9a3ca-114">Specifies the version of the remote engine to use.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a3ca-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a3ca-115">Return value</span></span>

<span data-ttu-id="9a3ca-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9a3ca-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a3ca-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9a3ca-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a3ca-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a3ca-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9a3ca-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9a3ca-119">Header</span></span></p></td><td><span data-ttu-id="9a3ca-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9a3ca-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9a3ca-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a3ca-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9a3ca-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="9a3ca-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
