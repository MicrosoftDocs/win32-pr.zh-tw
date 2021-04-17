---
title: 'IADsTimestamp 屬性方法 (Iads .h) '
description: IADsTimestamp 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- IADsTimestamp 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465061"
---
# <a name="iadstimestamp-property-methods"></a><span data-ttu-id="f21f9-105">IADsTimestamp 屬性方法</span><span class="sxs-lookup"><span data-stu-id="f21f9-105">IADsTimestamp Property Methods</span></span>

<span data-ttu-id="f21f9-106">[**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="f21f9-106">The property method of the [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) interface sets the property described in the following table.</span></span> <span data-ttu-id="f21f9-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="f21f9-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f21f9-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f21f9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f21f9-109">**EventID**</span><span class="sxs-lookup"><span data-stu-id="f21f9-109">**EventID**</span></span>
<span data-ttu-id="f21f9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f21f9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f21f9-111">事件識別項。</span><span class="sxs-lookup"><span data-stu-id="f21f9-111">An event identifier.</span></span>

<dt>

<span data-ttu-id="f21f9-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f21f9-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f21f9-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f21f9-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f21f9-114">**WholeSeconds**</span><span class="sxs-lookup"><span data-stu-id="f21f9-114">**WholeSeconds**</span></span>
<span data-ttu-id="f21f9-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f21f9-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f21f9-116">值為零的秒數，以12:00 為單位，UTC 時間為1970。</span><span class="sxs-lookup"><span data-stu-id="f21f9-116">Number of seconds with zero value being 12:00 AM, January 1970, UTC.</span></span>

<dt>

<span data-ttu-id="f21f9-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f21f9-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f21f9-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f21f9-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="f21f9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f21f9-119">Requirements</span></span>



| <span data-ttu-id="f21f9-120">需求</span><span class="sxs-lookup"><span data-stu-id="f21f9-120">Requirement</span></span> | <span data-ttu-id="f21f9-121">值</span><span class="sxs-lookup"><span data-stu-id="f21f9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f21f9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f21f9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f21f9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f21f9-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f21f9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f21f9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f21f9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f21f9-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f21f9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f21f9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f21f9-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="f21f9-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f21f9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f21f9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f21f9-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f21f9-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f21f9-130">IID</span><span class="sxs-lookup"><span data-stu-id="f21f9-130">IID</span></span><br/>                      | <span data-ttu-id="f21f9-131">IID \_ IADsTimestamp 定義為 B2F5A901-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="f21f9-131">IID\_IADsTimestamp is defined as B2F5A901-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f21f9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f21f9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21f9-133">**IADsTimestamp**</span><span class="sxs-lookup"><span data-stu-id="f21f9-133">**IADsTimestamp**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[<span data-ttu-id="f21f9-134">**ADS \_ 時間戳記**</span><span class="sxs-lookup"><span data-stu-id="f21f9-134">**ADS\_TIMESTAMP**</span></span>](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





