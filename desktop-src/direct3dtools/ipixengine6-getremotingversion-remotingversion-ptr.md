---
description: 取得引擎的遠端處理版本。
MS-HAID: vspixengine.IPixEngine6\_GetRemotingVersion\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine6：： GetRemotingVersion 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 065FC3A7-ECFB-4551-B4B0-CA0E6B8676F8
api_name:
- IPixEngine6.GetRemotingVersion
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85230a71d9c0f2dd437ec25af3eb6c660f032586
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025720"
---
# <a name="span-idvspixengineipixengine6_getremotingversion_remotingversion_ptrspanipixengine6getremotingversion-method"></a><span data-ttu-id="f5bf6-103"><span id="vspixengine.ipixengine6_getremotingversion_remotingversion_ptr"></span>IPixEngine6：： GetRemotingVersion 方法</span><span class="sxs-lookup"><span data-stu-id="f5bf6-103"><span id="vspixengine.ipixengine6_getremotingversion_remotingversion_ptr"></span>IPixEngine6::GetRemotingVersion method</span></span>

<span data-ttu-id="f5bf6-104">取得引擎的遠端處理版本。</span><span class="sxs-lookup"><span data-stu-id="f5bf6-104">Gets the remoting version of the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bf6-105">語法</span><span class="sxs-lookup"><span data-stu-id="f5bf6-105">Syntax</span></span>


```C++
HRESULT GetRemotingVersion(
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="f5bf6-106">參數</span><span class="sxs-lookup"><span data-stu-id="f5bf6-106">Parameters</span></span>

<span data-ttu-id="f5bf6-107">*pRemoteVersion* </span><span class="sxs-lookup"><span data-stu-id="f5bf6-107">*pRemoteVersion* </span></span>  
<span data-ttu-id="f5bf6-108">引擎的遠端處理版本。</span><span class="sxs-lookup"><span data-stu-id="f5bf6-108">The remoting version of the engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5bf6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5bf6-109">Return value</span></span>

<span data-ttu-id="f5bf6-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f5bf6-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5bf6-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f5bf6-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bf6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5bf6-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f5bf6-113">標頭</span><span class="sxs-lookup"><span data-stu-id="f5bf6-113">Header</span></span></p></td><td><span data-ttu-id="f5bf6-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="f5bf6-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f5bf6-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5bf6-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f5bf6-116">**IPixEngine6**</span><span class="sxs-lookup"><span data-stu-id="f5bf6-116">**IPixEngine6**</span></span>](/windows/desktop/direct3dtools/ipixengine6)

 

 
