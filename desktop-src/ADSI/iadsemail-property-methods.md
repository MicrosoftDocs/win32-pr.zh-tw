---
title: 'IADsEmail 屬性方法 (Iads .h) '
description: IADsEmail 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- IADsEmail 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385069"
---
# <a name="iadsemail-property-methods"></a><span data-ttu-id="c1f55-105">IADsEmail 屬性方法</span><span class="sxs-lookup"><span data-stu-id="c1f55-105">IADsEmail Property Methods</span></span>

<span data-ttu-id="c1f55-106">[**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1f55-106">The property method of the [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) interface sets the property described in the following table.</span></span> <span data-ttu-id="c1f55-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="c1f55-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c1f55-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c1f55-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c1f55-109">**位址**</span><span class="sxs-lookup"><span data-stu-id="c1f55-109">**Address**</span></span>
<span data-ttu-id="c1f55-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c1f55-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c1f55-111">使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="c1f55-111">The email address of the user.</span></span>

<dt>

<span data-ttu-id="c1f55-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c1f55-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c1f55-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c1f55-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1f55-114">**型別**</span><span class="sxs-lookup"><span data-stu-id="c1f55-114">**Type**</span></span>
<span data-ttu-id="c1f55-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c1f55-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c1f55-116">電子郵件訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="c1f55-116">The type of the email message.</span></span>

<dt>

<span data-ttu-id="c1f55-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c1f55-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c1f55-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="c1f55-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="c1f55-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1f55-119">Requirements</span></span>



| <span data-ttu-id="c1f55-120">需求</span><span class="sxs-lookup"><span data-stu-id="c1f55-120">Requirement</span></span> | <span data-ttu-id="c1f55-121">值</span><span class="sxs-lookup"><span data-stu-id="c1f55-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f55-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1f55-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1f55-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1f55-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1f55-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1f55-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1f55-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1f55-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1f55-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c1f55-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1f55-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1f55-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c1f55-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c1f55-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1f55-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1f55-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1f55-130">IID</span><span class="sxs-lookup"><span data-stu-id="c1f55-130">IID</span></span><br/>                      | <span data-ttu-id="c1f55-131">IID \_ IADsEmail 定義為97AF011A-478E-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="c1f55-131">IID\_IADsEmail is defined as 97AF011A-478E-11D1-A3B4-00C04FB950DC</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c1f55-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1f55-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f55-133">**IADsEmail**</span><span class="sxs-lookup"><span data-stu-id="c1f55-133">**IADsEmail**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[<span data-ttu-id="c1f55-134">**ADS \_ 電子郵件**</span><span class="sxs-lookup"><span data-stu-id="c1f55-134">**ADS\_EMAIL**</span></span>](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





