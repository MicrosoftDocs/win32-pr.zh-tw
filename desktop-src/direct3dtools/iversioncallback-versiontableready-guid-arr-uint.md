---
description: 回呼函式，用來通知主機支援的介面。
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IVersionCallback：： VersionTableReady 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4f31f8b4619d74f6f491f6be8faf7ddd457ee82c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109296"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span data-ttu-id="1bf17-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback：： VersionTableReady 方法</span><span class="sxs-lookup"><span data-stu-id="1bf17-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady method</span></span>

<span data-ttu-id="1bf17-104">回呼函式，用來通知主機支援的介面。</span><span class="sxs-lookup"><span data-stu-id="1bf17-104">A callback function used to notify the host of which interfaces are supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf17-105">語法</span><span class="sxs-lookup"><span data-stu-id="1bf17-105">Syntax</span></span>


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a><span data-ttu-id="1bf17-106">參數</span><span class="sxs-lookup"><span data-stu-id="1bf17-106">Parameters</span></span>

<span data-ttu-id="1bf17-107">*count1 \_ interfaceIds* </span><span class="sxs-lookup"><span data-stu-id="1bf17-107">*count1\_interfaceIds* </span></span>  
<span data-ttu-id="1bf17-108">陣列，其中包含支援之介面識別碼的 Guid。</span><span class="sxs-lookup"><span data-stu-id="1bf17-108">An array containing the GUIDs of supported interface IDs.</span></span>

<span data-ttu-id="1bf17-109">*計數* </span><span class="sxs-lookup"><span data-stu-id="1bf17-109">*count* </span></span>  
<span data-ttu-id="1bf17-110">傳遞至 count1 interfaceIds 的 Guid 數目 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1bf17-110">The number of GUIDs passed in count1\_interfaceIds.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bf17-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bf17-111">Return value</span></span>

<span data-ttu-id="1bf17-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1bf17-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1bf17-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1bf17-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf17-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bf17-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1bf17-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1bf17-115">Header</span></span></p></td><td><span data-ttu-id="1bf17-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="1bf17-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1bf17-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bf17-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1bf17-118">**IVersionCallback**</span><span class="sxs-lookup"><span data-stu-id="1bf17-118">**IVersionCallback**</span></span>](/windows/desktop/direct3dtools/iversioncallback)

 

 
