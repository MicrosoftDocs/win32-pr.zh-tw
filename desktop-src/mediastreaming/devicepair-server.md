---
title: 'DevicePair 伺服器屬性 (Asptlb .h) '
description: 取得 active basic 裝置配對的伺服器。
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- 伺服器屬性媒體串流 API
- 伺服器屬性媒體串流 API，DevicePair 介面
- DevicePair 介面媒體串流 API，伺服器屬性
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977144"
---
# <a name="devicepairserver-property"></a><span data-ttu-id="38847-106">DevicePair：： Server 屬性</span><span class="sxs-lookup"><span data-stu-id="38847-106">DevicePair::Server property</span></span>

<span data-ttu-id="38847-107">取得 active basic 裝置配對的伺服器。</span><span class="sxs-lookup"><span data-stu-id="38847-107">Gets the server for the active basic device pair.</span></span>

<span data-ttu-id="38847-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="38847-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="38847-109">語法</span><span class="sxs-lookup"><span data-stu-id="38847-109">Syntax</span></span>


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="38847-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="38847-110">Property value</span></span>

<span data-ttu-id="38847-111">接收代表伺服器裝置的 [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="38847-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the server device.</span></span>

## <a name="requirements"></a><span data-ttu-id="38847-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="38847-112">Requirements</span></span>



| <span data-ttu-id="38847-113">需求</span><span class="sxs-lookup"><span data-stu-id="38847-113">Requirement</span></span> | <span data-ttu-id="38847-114">值</span><span class="sxs-lookup"><span data-stu-id="38847-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="38847-115">標頭</span><span class="sxs-lookup"><span data-stu-id="38847-115">Header</span></span><br/> | <dl> <span data-ttu-id="38847-116"><dt>Asptlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="38847-116"><dt>Asptlb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38847-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38847-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="38847-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38847-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

