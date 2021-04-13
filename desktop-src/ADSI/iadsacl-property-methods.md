---
title: 'IADsAcl 屬性方法 (Iads .h) '
description: IADsAcl 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- IADsAcl 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466248"
---
# <a name="iadsacl-property-methods"></a><span data-ttu-id="44f5d-105">IADsAcl 屬性方法</span><span class="sxs-lookup"><span data-stu-id="44f5d-105">IADsAcl Property Methods</span></span>

<span data-ttu-id="44f5d-106">[**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="44f5d-106">The property method of the [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) interface sets the property described in the following table.</span></span> <span data-ttu-id="44f5d-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="44f5d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="44f5d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="44f5d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="44f5d-109">**特權**</span><span class="sxs-lookup"><span data-stu-id="44f5d-109">**Privileges**</span></span>
<span data-ttu-id="44f5d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="44f5d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="44f5d-111">許可權設定。</span><span class="sxs-lookup"><span data-stu-id="44f5d-111">Privilege settings.</span></span>

<dt>

<span data-ttu-id="44f5d-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="44f5d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="44f5d-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="44f5d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f5d-114">**ProtectedAttrName**</span><span class="sxs-lookup"><span data-stu-id="44f5d-114">**ProtectedAttrName**</span></span>
<span data-ttu-id="44f5d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="44f5d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="44f5d-116">受保護屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="44f5d-116">Name of a protected attribute.</span></span>

<dt>

<span data-ttu-id="44f5d-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="44f5d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="44f5d-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="44f5d-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f5d-119">**SubjectName**</span><span class="sxs-lookup"><span data-stu-id="44f5d-119">**SubjectName**</span></span>
<span data-ttu-id="44f5d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="44f5d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="44f5d-121">主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="44f5d-121">Name of the subject.</span></span>

<dt>

<span data-ttu-id="44f5d-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="44f5d-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="44f5d-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="44f5d-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="44f5d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="44f5d-124">Requirements</span></span>



| <span data-ttu-id="44f5d-125">需求</span><span class="sxs-lookup"><span data-stu-id="44f5d-125">Requirement</span></span> | <span data-ttu-id="44f5d-126">值</span><span class="sxs-lookup"><span data-stu-id="44f5d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44f5d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44f5d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="44f5d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44f5d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44f5d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44f5d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="44f5d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44f5d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44f5d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="44f5d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f5d-132"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="44f5d-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="44f5d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="44f5d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44f5d-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44f5d-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="44f5d-135">IID</span><span class="sxs-lookup"><span data-stu-id="44f5d-135">IID</span></span><br/>                      | <span data-ttu-id="44f5d-136">IID \_ IADsAcl 定義為8452D3AB-0869-11D1-A377-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="44f5d-136">IID\_IADsAcl is defined as 8452D3AB-0869-11D1-A377-00C04FB950DC</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="44f5d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44f5d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f5d-138">**IADsAcl**</span><span class="sxs-lookup"><span data-stu-id="44f5d-138">**IADsAcl**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





