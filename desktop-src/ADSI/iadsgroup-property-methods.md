---
title: 'IADsGroup 屬性方法 (Iads .h) '
description: IADsGroup 介面的屬性方法。
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- IADsGroup 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965508"
---
# <a name="iadsgroup-property-methods"></a><span data-ttu-id="2d5fd-104">IADsGroup 屬性方法</span><span class="sxs-lookup"><span data-stu-id="2d5fd-104">IADsGroup Property Methods</span></span>

<span data-ttu-id="2d5fd-105">[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)介面的屬性方法會讀取並寫入下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-105">The property methods of the [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) interface read and write the following properties.</span></span> <span data-ttu-id="2d5fd-106">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="2d5fd-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2d5fd-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="2d5fd-108">**說明**</span><span class="sxs-lookup"><span data-stu-id="2d5fd-108">**Description**</span></span>
<span data-ttu-id="2d5fd-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="2d5fd-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="2d5fd-110">指出群組成員資格的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-110">Indicates the textual description of the group membership.</span></span>

<dt>

<span data-ttu-id="2d5fd-111">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d5fd-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2d5fd-112">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2d5fd-112">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="2d5fd-113">備註</span><span class="sxs-lookup"><span data-stu-id="2d5fd-113">Remarks</span></span>

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a><span data-ttu-id="2d5fd-114">使用 IADsGroup 來取出內建組的描述</span><span class="sxs-lookup"><span data-stu-id="2d5fd-114">Using IADsGroup to Retrieve Descriptions of Built-in Groups</span></span>

<span data-ttu-id="2d5fd-115">下列範例示範如何依名稱抓取 Windows 群組物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-115">The following examples show how to retrieve information about Windows group objects by name.</span></span> <span data-ttu-id="2d5fd-116">在多國語言環境中，內建組有時候是由不同的當地語系化名稱所知道，這表示無法使用 "WinNT://Microsoft/Administrators" 之類的字串識別碼直接取出它們。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-116">In a multilingual environment, built-in groups are sometimes known by different localized names, which means that they cannot be retrieved directly by using string identifiers such as "WinNT://Microsoft/Administrators".</span></span> <span data-ttu-id="2d5fd-117">在這種情況下，使用者可以系結至該群組已知的 SID 物件、取出當地語系化的組名，然後將其提供給 GetObject 方法。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-117">In that case, the user can bind to the well-known SID object for the group, retrieve the localized group name, and supply that to the GetObject method.</span></span> <span data-ttu-id="2d5fd-118">如需詳細資訊，請參閱 [知名的 sid](/windows/desktop/SecAuthZ/well-known-sids)。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-118">For more information, see [Well-known SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span></span>

## <a name="examples"></a><span data-ttu-id="2d5fd-119">範例</span><span class="sxs-lookup"><span data-stu-id="2d5fd-119">Examples</span></span>

<span data-ttu-id="2d5fd-120">下列 Visual Basic 範例顯示如何系結至群組物件，並顯示群組的描述。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-120">The following Visual Basic example shows how to bind to a group object and display the description of the group.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="2d5fd-121">下列 c + + 範例顯示如何系結至群組物件，並顯示群組的描述。</span><span class="sxs-lookup"><span data-stu-id="2d5fd-121">The following C++ example shows how to bind to a group object and display the description of the group.</span></span>


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a><span data-ttu-id="2d5fd-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d5fd-122">Requirements</span></span>



| <span data-ttu-id="2d5fd-123">需求</span><span class="sxs-lookup"><span data-stu-id="2d5fd-123">Requirement</span></span> | <span data-ttu-id="2d5fd-124">值</span><span class="sxs-lookup"><span data-stu-id="2d5fd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5fd-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d5fd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d5fd-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d5fd-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d5fd-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d5fd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d5fd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d5fd-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d5fd-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2d5fd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d5fd-130"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d5fd-130"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="2d5fd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2d5fd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d5fd-132"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d5fd-132"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="2d5fd-133">IID</span><span class="sxs-lookup"><span data-stu-id="2d5fd-133">IID</span></span><br/>                      | <span data-ttu-id="2d5fd-134">IID \_ IADsGroup 定義為27636B00-410F-11CF-B1FF-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="2d5fd-134">IID\_IADsGroup is defined as 27636B00-410F-11CF-B1FF-02608C9E7553</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2d5fd-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d5fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5fd-136">**IADs**</span><span class="sxs-lookup"><span data-stu-id="2d5fd-136">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="2d5fd-137">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="2d5fd-137">**IADsGroup**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="2d5fd-138">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="2d5fd-138">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

