---
title: 'IADsPropertyList 屬性方法 (Iads .h) '
description: IADsPropertyList 介面的屬性方法會讀取下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 3564b61a-5950-4d00-8ea1-86fecd5c6c4e
ms.tgt_platform: multiple
keywords:
- IADsPropertyList 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPropertyList Property Methods
- IADsPropertyList.PropertyCount
- IADsPropertyList.get_PropertyCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f13494eeb502122216ffa0c73c24d5b707588e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844291"
---
# <a name="iadspropertylist-property-methods"></a><span data-ttu-id="44e34-105">IADsPropertyList 屬性方法</span><span class="sxs-lookup"><span data-stu-id="44e34-105">IADsPropertyList Property Methods</span></span>

<span data-ttu-id="44e34-106">[**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)介面的屬性方法會讀取下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="44e34-106">The property methods of the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface read the properties described in the following table.</span></span> <span data-ttu-id="44e34-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="44e34-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="44e34-108">屬性</span><span class="sxs-lookup"><span data-stu-id="44e34-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="44e34-109">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="44e34-109">**PropertyCount**</span></span>
<span data-ttu-id="44e34-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="44e34-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="44e34-111">屬性清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="44e34-111">The number of items in the property list.</span></span>

<dt>

<span data-ttu-id="44e34-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44e34-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e34-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="44e34-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PropertyCount(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="44e34-114">範例</span><span class="sxs-lookup"><span data-stu-id="44e34-114">Examples</span></span>

<span data-ttu-id="44e34-115">下列程式碼範例顯示如何判斷屬性清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="44e34-115">The following code example shows how to determine number of items in a property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim count As Long

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
count = propList.PropertyCount
Debug.Print "Number of Properties Found: " & count

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
```



<span data-ttu-id="44e34-116">下列程式碼範例顯示如何判斷屬性清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="44e34-116">The following code example shows how to determine number of items in a property list.</span></span>


```C++
int GetPropertyCacheCount(LPWSTR adsPath)
{
    IADsPropertyList *pList;
    IADs *pObj;
    HRESULT hr = S_OK;

    if(!adsPath)
    {
        _tprintf(TEXT("Invalid ADsPath."));
        return -1;
    }

    HRESULT hr = ADsGetObject(adsPath,
                          IID_IADsPropertyList,
                          (void**)&pList);
    // Initialize the property cache.
    hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
    pObj->GetInfo();
    pObj->Release();

    // Get the property count.
    hr = pList->get_PropertyCount(&count);
    pList->Release();

    // Return the property count if it succeeded, otherwise
    // return -1.

    if(SUCCEEDED(hr))
    {
        return count;
    }
    else
    {
        return -1;
    }

}
```



## <a name="requirements"></a><span data-ttu-id="44e34-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="44e34-117">Requirements</span></span>



| <span data-ttu-id="44e34-118">需求</span><span class="sxs-lookup"><span data-stu-id="44e34-118">Requirement</span></span> | <span data-ttu-id="44e34-119">值</span><span class="sxs-lookup"><span data-stu-id="44e34-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44e34-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44e34-120">Minimum supported client</span></span><br/> | <span data-ttu-id="44e34-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44e34-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44e34-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44e34-122">Minimum supported server</span></span><br/> | <span data-ttu-id="44e34-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44e34-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44e34-124">標頭</span><span class="sxs-lookup"><span data-stu-id="44e34-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e34-125"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="44e34-125"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="44e34-126">DLL</span><span class="sxs-lookup"><span data-stu-id="44e34-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44e34-127"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44e34-127"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="44e34-128">IID</span><span class="sxs-lookup"><span data-stu-id="44e34-128">IID</span></span><br/>                      | <span data-ttu-id="44e34-129">IID \_ IADsPropertyList 定義為 C6F602B6-8F69-11D0-8528-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="44e34-129">IID\_IADsPropertyList is defined as C6F602B6-8F69-11D0-8528-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="44e34-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44e34-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e34-131">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="44e34-131">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="44e34-132">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="44e34-132">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





