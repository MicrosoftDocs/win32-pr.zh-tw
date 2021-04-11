---
title: 'IADsNameTranslate 屬性方法 (Iads .h) '
description: 設定 ChaseReferral 屬性。
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- IADsNameTranslate 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934815"
---
# <a name="iadsnametranslate-property-methods"></a><span data-ttu-id="a878e-104">IADsNameTranslate 屬性方法</span><span class="sxs-lookup"><span data-stu-id="a878e-104">IADsNameTranslate Property Methods</span></span>

<span data-ttu-id="a878e-105">[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)介面的 property 方法會設定 **ChaseReferral** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a878e-105">The property method of the [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface sets the **ChaseReferral** property.</span></span> <span data-ttu-id="a878e-106">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="a878e-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a878e-107">屬性</span><span class="sxs-lookup"><span data-stu-id="a878e-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a878e-108">**ChaseReferral**</span><span class="sxs-lookup"><span data-stu-id="a878e-108">**ChaseReferral**</span></span>
<span data-ttu-id="a878e-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a878e-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="a878e-110">在 ADS 中定義的參考追蹤選項會追蹤 [**\_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)。</span><span class="sxs-lookup"><span data-stu-id="a878e-110">Options of referral chasing as defined in [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span></span> <span data-ttu-id="a878e-111">設定參考追蹤時，會在不屬於這個目錄的物件上執行名稱轉譯，而這些物件則是從參考追蹤傳回的參考。</span><span class="sxs-lookup"><span data-stu-id="a878e-111">When referral chasing is set, the name translation is performed on objects that do not belong to this directory and are the referrals returned from referral chasing.</span></span>

<dt>

<span data-ttu-id="a878e-112">存取類型：僅限寫入</span><span class="sxs-lookup"><span data-stu-id="a878e-112">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="a878e-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="a878e-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="a878e-114">備註</span><span class="sxs-lookup"><span data-stu-id="a878e-114">Remarks</span></span>

<span data-ttu-id="a878e-115">只有當您使用 [**IADsNameTranslate：： Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) 和 [**IADsNameTranslate：： Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)時，才適用參考追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="a878e-115">The referral chasing options apply only when you use [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) and [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span></span> <span data-ttu-id="a878e-116">[**IADsNameTranslate：： SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)或 [**IADsNameTranslate：： GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)無法使用此功能。</span><span class="sxs-lookup"><span data-stu-id="a878e-116">The feature is not available with [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) or [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span></span>

<span data-ttu-id="a878e-117">[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)介面具有部分實作為廣告的部分執行，會透過 **ChaseReferral** 屬性來進行 [**\_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)。</span><span class="sxs-lookup"><span data-stu-id="a878e-117">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface has a partial implementation of [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) through the **ChaseReferral** property.</span></span> <span data-ttu-id="a878e-118">如果 [ **ChaseReferral** ] 屬性設定為 [零] (0) ，則與指定廣告的 [ **\_ \_ \_ 永遠不** (0) ] 相同。</span><span class="sxs-lookup"><span data-stu-id="a878e-118">If the **ChaseReferral** property is set to zero (0), it is the same as specifying **ADS\_CHASE\_REFERRALS\_NEVER** (0).</span></span> <span data-ttu-id="a878e-119">如果使用非零值，則與指定 **廣告 \_ \_ \_ 一律** (0x60) 相同。</span><span class="sxs-lookup"><span data-stu-id="a878e-119">If a nonzero value is used, it is the same as specifying **ADS\_CHASE\_REFERRALS\_ALWAYS** (0x60).</span></span> <span data-ttu-id="a878e-120">**IADsNameTranslate** 不會執行 **廣告將 \_ \_ 參考 \_ 附屬** (0x20) 或 ADS 會 (0x40) 選項來進行 **\_ \_ 參考 \_** 。</span><span class="sxs-lookup"><span data-stu-id="a878e-120">**IADsNameTranslate** does not implement the **ADS\_CHASE\_REFERRALS\_SUBORDINATE** (0x20) or **ADS\_CHASE\_REFERRALS\_EXTERNAL** (0x40) options.</span></span>

<span data-ttu-id="a878e-121">已啟用參考追蹤的預設設定 (**ADS 會 \_ \_ \_ 一律**) 。</span><span class="sxs-lookup"><span data-stu-id="a878e-121">The default setting for referral chasing is enabled (**ADS\_CHASE\_REFERRALS\_ALWAYS**).</span></span> <span data-ttu-id="a878e-122">如果沒有參考追蹤，您可以在僅限連線目錄伺服器的物件上執行名稱轉譯。</span><span class="sxs-lookup"><span data-stu-id="a878e-122">Without referral chasing, you can have name translation performed on those objects residing on the connected directory server only.</span></span> <span data-ttu-id="a878e-123">如果您不確定感興趣的物件是否在指定的伺服器上，您應該將此屬性設定為 **ADS \_ \_ \_ 一律** 會進行參考。</span><span class="sxs-lookup"><span data-stu-id="a878e-123">If you are uncertain whether the object of interest is on the specified server, you should set this property to be **ADS\_CHASE\_REFERRALS\_ALWAYS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a878e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a878e-124">Requirements</span></span>



| <span data-ttu-id="a878e-125">需求</span><span class="sxs-lookup"><span data-stu-id="a878e-125">Requirement</span></span> | <span data-ttu-id="a878e-126">值</span><span class="sxs-lookup"><span data-stu-id="a878e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a878e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a878e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a878e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a878e-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a878e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a878e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a878e-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a878e-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a878e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a878e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a878e-132"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="a878e-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="a878e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a878e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a878e-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a878e-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="a878e-135">IID</span><span class="sxs-lookup"><span data-stu-id="a878e-135">IID</span></span><br/>                      | <span data-ttu-id="a878e-136">IID \_ IADsNameTranslate 定義為 B1B272A3-3625-11D1-A3A4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="a878e-136">IID\_IADsNameTranslate is defined as B1B272A3-3625-11D1-A3A4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a878e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a878e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a878e-138">**廣告會將 \_ \_ 參考 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="a878e-138">**ADS\_CHASE\_REFERRALS\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[<span data-ttu-id="a878e-139">**IADsNameTranslate**</span><span class="sxs-lookup"><span data-stu-id="a878e-139">**IADsNameTranslate**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[<span data-ttu-id="a878e-140">**IADsNameTranslate：： Get**</span><span class="sxs-lookup"><span data-stu-id="a878e-140">**IADsNameTranslate::Get**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[<span data-ttu-id="a878e-141">**IADsNameTranslate::GetEx**</span><span class="sxs-lookup"><span data-stu-id="a878e-141">**IADsNameTranslate::GetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[<span data-ttu-id="a878e-142">**IADsNameTranslate：： Set**</span><span class="sxs-lookup"><span data-stu-id="a878e-142">**IADsNameTranslate::Set**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[<span data-ttu-id="a878e-143">**IADsNameTranslate::SetEx**</span><span class="sxs-lookup"><span data-stu-id="a878e-143">**IADsNameTranslate::SetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[<span data-ttu-id="a878e-144">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="a878e-144">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





