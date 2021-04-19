---
title: 'IADsMembers 屬性方法 (Iads .h) '
description: IADsMembers 介面的方法會讀取及寫入本主題中所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- IADsMembers 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969607"
---
# <a name="iadsmembers-property-methods"></a><span data-ttu-id="82d0a-105">IADsMembers 屬性方法</span><span class="sxs-lookup"><span data-stu-id="82d0a-105">IADsMembers Property Methods</span></span>

<span data-ttu-id="82d0a-106">[**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)介面的方法會讀取及寫入本主題中所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="82d0a-106">The methods of the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="82d0a-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="82d0a-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="82d0a-108">屬性</span><span class="sxs-lookup"><span data-stu-id="82d0a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="82d0a-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="82d0a-109">**Count**</span></span>
<span data-ttu-id="82d0a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="82d0a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="82d0a-111">指出容器中的專案數目。</span><span class="sxs-lookup"><span data-stu-id="82d0a-111">Indicates the number of items in the container.</span></span> <span data-ttu-id="82d0a-112">如果設定篩選準則，則 count 只會傳回符合篩選描述的專案數目。</span><span class="sxs-lookup"><span data-stu-id="82d0a-112">If the filter is set then count returns only the number of items that fit the filter description.</span></span>

<dt>

<span data-ttu-id="82d0a-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82d0a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d0a-114">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="82d0a-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="82d0a-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="82d0a-115">**Filter**</span></span>
<span data-ttu-id="82d0a-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="82d0a-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="82d0a-117">表示篩選。</span><span class="sxs-lookup"><span data-stu-id="82d0a-117">Indicates the filter.</span></span> <span data-ttu-id="82d0a-118">篩選陣列中專案的語法與 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面上所使用的篩選器相同。</span><span class="sxs-lookup"><span data-stu-id="82d0a-118">The syntax of the entries in the filter array is the same as the Filter used on the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span>

<dt>

<span data-ttu-id="82d0a-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="82d0a-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="82d0a-120">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="82d0a-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="82d0a-121">備註</span><span class="sxs-lookup"><span data-stu-id="82d0a-121">Remarks</span></span>

<span data-ttu-id="82d0a-122">ADSI 系統提供者不支援 **IADsMembers：： get \_ Count** 屬性方法。</span><span class="sxs-lookup"><span data-stu-id="82d0a-122">The ADSI system providers do not support the **IADsMembers::get\_Count** property method.</span></span>

## <a name="examples"></a><span data-ttu-id="82d0a-123">範例</span><span class="sxs-lookup"><span data-stu-id="82d0a-123">Examples</span></span>

<span data-ttu-id="82d0a-124">下列程式碼範例示範如何使用這個介面的屬性方法。</span><span class="sxs-lookup"><span data-stu-id="82d0a-124">The following code example shows how to use the property methods of this interface.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="82d0a-125">下列程式碼範例使用 **IADsMembers：:p ui \_ 篩選** 方法來準備群組成員集合的列舉。</span><span class="sxs-lookup"><span data-stu-id="82d0a-125">The following code example uses the **IADsMembers::put\_Filter** method to prepare for an enumeration of the collection of members of a group.</span></span>


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="82d0a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="82d0a-126">Requirements</span></span>



| <span data-ttu-id="82d0a-127">需求</span><span class="sxs-lookup"><span data-stu-id="82d0a-127">Requirement</span></span> | <span data-ttu-id="82d0a-128">值</span><span class="sxs-lookup"><span data-stu-id="82d0a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82d0a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82d0a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="82d0a-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82d0a-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82d0a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82d0a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="82d0a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82d0a-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82d0a-133">標頭</span><span class="sxs-lookup"><span data-stu-id="82d0a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="82d0a-134"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="82d0a-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="82d0a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="82d0a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d0a-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d0a-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="82d0a-137">IID</span><span class="sxs-lookup"><span data-stu-id="82d0a-137">IID</span></span><br/>                      | <span data-ttu-id="82d0a-138">IID \_ IADsMembers 定義為451A0030-72EC-11CF-B03B-00AA006E0975</span><span class="sxs-lookup"><span data-stu-id="82d0a-138">IID\_IADsMembers is defined as 451A0030-72EC-11CF-B03B-00AA006E0975</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="82d0a-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82d0a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d0a-140">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="82d0a-140">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="82d0a-141">**IADsMembers：： get \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="82d0a-141">**IADsMembers::get\_\_NewEnum**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[<span data-ttu-id="82d0a-142">**IADsMembers**</span><span class="sxs-lookup"><span data-stu-id="82d0a-142">**IADsMembers**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[<span data-ttu-id="82d0a-143">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="82d0a-143">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





