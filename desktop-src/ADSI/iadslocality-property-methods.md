---
title: 'IADsLocality 屬性方法 (Iads .h) '
description: IADsLocality 介面的方法會讀取及寫入本主題中所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- IADsLocality 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34023f0af5365deb4f023d53a843dcf688c40afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934817"
---
# <a name="iadslocality-property-methods"></a><span data-ttu-id="d207f-105">IADsLocality 屬性方法</span><span class="sxs-lookup"><span data-stu-id="d207f-105">IADsLocality Property Methods</span></span>

<span data-ttu-id="d207f-106">[**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)介面的方法會讀取及寫入本主題中所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="d207f-106">The methods of the [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="d207f-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="d207f-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d207f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="d207f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d207f-109">**說明**</span><span class="sxs-lookup"><span data-stu-id="d207f-109">**Description**</span></span>
<span data-ttu-id="d207f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d207f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d207f-111">指出描述位置的文字。</span><span class="sxs-lookup"><span data-stu-id="d207f-111">Indicates the text that describes the locality.</span></span>

<dt>

<span data-ttu-id="d207f-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d207f-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d207f-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d207f-113">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> <dt>

<span data-ttu-id="d207f-114">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="d207f-114">**LocalityName**</span></span>
<span data-ttu-id="d207f-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d207f-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d207f-116">表示此位置物件所表示之地理區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="d207f-116">Indicates the name of the geographical region as represented by this locality object.</span></span>

<dt>

<span data-ttu-id="d207f-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d207f-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d207f-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d207f-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d207f-119">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="d207f-119">**PostalAddress**</span></span>
<span data-ttu-id="d207f-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d207f-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d207f-121">表示位置的主要郵遞區號位址。</span><span class="sxs-lookup"><span data-stu-id="d207f-121">Indicates the main postal address of the locality.</span></span>

<dt>

<span data-ttu-id="d207f-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d207f-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d207f-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d207f-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d207f-124">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="d207f-124">**SeeAlso**</span></span>
<span data-ttu-id="d207f-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d207f-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="d207f-126">指出與這個物件相關之目錄物件的 ADsPath 名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="d207f-126">Indicates an array of ADsPath names of directory objects relevant to this object.</span></span>

<dt>

<span data-ttu-id="d207f-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d207f-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d207f-128">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="d207f-128">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d207f-129">範例</span><span class="sxs-lookup"><span data-stu-id="d207f-129">Examples</span></span>

<span data-ttu-id="d207f-130">下列程式碼範例會顯示容器物件的位置資料。</span><span class="sxs-lookup"><span data-stu-id="d207f-130">The following code example displays the locality data of a container object.</span></span> <span data-ttu-id="d207f-131">它會假設已為容器物件建立名為 "myLocality" 的位置物件，且已設定屬性。</span><span class="sxs-lookup"><span data-stu-id="d207f-131">It assumes that a locality object, named "myLocality", has been created for the container object and the properties have been set.</span></span>


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a><span data-ttu-id="d207f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d207f-132">Requirements</span></span>



| <span data-ttu-id="d207f-133">需求</span><span class="sxs-lookup"><span data-stu-id="d207f-133">Requirement</span></span> | <span data-ttu-id="d207f-134">值</span><span class="sxs-lookup"><span data-stu-id="d207f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d207f-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d207f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d207f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d207f-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d207f-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d207f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d207f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d207f-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d207f-139">標頭</span><span class="sxs-lookup"><span data-stu-id="d207f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d207f-140"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="d207f-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d207f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d207f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d207f-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d207f-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d207f-143">IID</span><span class="sxs-lookup"><span data-stu-id="d207f-143">IID</span></span><br/>                      | <span data-ttu-id="d207f-144">IID \_ IADsLocality 定義為 A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="d207f-144">IID\_IADsLocality is defined as A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d207f-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d207f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d207f-146">**IADs**</span><span class="sxs-lookup"><span data-stu-id="d207f-146">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="d207f-147">**IADsLocality**</span><span class="sxs-lookup"><span data-stu-id="d207f-147">**IADsLocality**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[<span data-ttu-id="d207f-148">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="d207f-148">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





