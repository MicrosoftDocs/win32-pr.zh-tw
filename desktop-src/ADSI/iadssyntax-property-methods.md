---
title: 'IADsSyntax 屬性方法 (Iads .h) '
description: IADsSyntax 介面的屬性方法會取得或設定下表所列的屬性。 如需屬性方法的詳細資訊，請參閱介面屬性方法。
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- IADsSyntax 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508495"
---
# <a name="iadssyntax-property-methods"></a><span data-ttu-id="f0bd8-105">IADsSyntax 屬性方法</span><span class="sxs-lookup"><span data-stu-id="f0bd8-105">IADsSyntax Property Methods</span></span>

<span data-ttu-id="f0bd8-106">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)介面的屬性方法會取得或設定下表所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-106">The property methods of the [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="f0bd8-107">如需屬性方法的詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f0bd8-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f0bd8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f0bd8-109">**OleAutoDataType**</span><span class="sxs-lookup"><span data-stu-id="f0bd8-109">**OleAutoDataType**</span></span>
<span data-ttu-id="f0bd8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f0bd8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f0bd8-111">抓取並設定 **LONG** ，其包含表示此語法之 Automation 資料類型的 **VT \_ xxx** 常數值。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-111">Retrieves and sets a **LONG** that contains the value of the **VT\_xxx** constant for the Automation data type that represents this syntax.</span></span>

<span data-ttu-id="f0bd8-112">Active Directory 針對表示此語法的 Automation 資料類型支援下列 **VT \_ xxx** 常數：</span><span class="sxs-lookup"><span data-stu-id="f0bd8-112">Active Directory supports the following **VT\_xxx** constants for the Automation data type that represents this syntax:</span></span>

-   <span data-ttu-id="f0bd8-113">**VT \_BOOL** BOOL</span><span class="sxs-lookup"><span data-stu-id="f0bd8-113">**VT\_BOOL** BOOL</span></span>
-   <span data-ttu-id="f0bd8-114">**VT \_BSTR** BSTR</span><span class="sxs-lookup"><span data-stu-id="f0bd8-114">**VT\_BSTR** BSTR</span></span>
-   <span data-ttu-id="f0bd8-115">**VT \_BSTRT** BSTRT</span><span class="sxs-lookup"><span data-stu-id="f0bd8-115">**VT\_BSTRT** BSTRT</span></span>
-   <span data-ttu-id="f0bd8-116">**VT \_CY** 貨幣</span><span class="sxs-lookup"><span data-stu-id="f0bd8-116">**VT\_CY** CURRENCY</span></span>
-   <span data-ttu-id="f0bd8-117">**VT \_日期** 日期</span><span class="sxs-lookup"><span data-stu-id="f0bd8-117">**VT\_DATE** Date</span></span>
-   <span data-ttu-id="f0bd8-118">**VT \_空白** **Null**</span><span class="sxs-lookup"><span data-stu-id="f0bd8-118">**VT\_EMPTY** **NULL**</span></span>
-   <span data-ttu-id="f0bd8-119">**VT \_錯誤** 無效</span><span class="sxs-lookup"><span data-stu-id="f0bd8-119">**VT\_ERROR** Not valid</span></span>
-   <span data-ttu-id="f0bd8-120">**VT \_I2** 簡短</span><span class="sxs-lookup"><span data-stu-id="f0bd8-120">**VT\_I2** short</span></span>
-   <span data-ttu-id="f0bd8-121">**VT \_I4** long</span><span class="sxs-lookup"><span data-stu-id="f0bd8-121">**VT\_I4** long</span></span>
-   <span data-ttu-id="f0bd8-122">**VT \_R4** real</span><span class="sxs-lookup"><span data-stu-id="f0bd8-122">**VT\_R4** real</span></span>
-   <span data-ttu-id="f0bd8-123">**VT \_R8** double</span><span class="sxs-lookup"><span data-stu-id="f0bd8-123">**VT\_R8** double</span></span>
-   <span data-ttu-id="f0bd8-124">**VT \_UI1** 位元組</span><span class="sxs-lookup"><span data-stu-id="f0bd8-124">**VT\_UI1** BYTE</span></span>

<dt>

<span data-ttu-id="f0bd8-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f0bd8-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f0bd8-126">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f0bd8-126">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="f0bd8-127">備註</span><span class="sxs-lookup"><span data-stu-id="f0bd8-127">Remarks</span></span>

<span data-ttu-id="f0bd8-128">不帶正負號的位元組陣列， **vt \_ UI1** \| **vt \_ array** 可能表示提供者已對應無法對應至 Automation 虛擬類型的語法。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-128">An array of unsigned bytes, **VT\_UI1**\|**VT\_ARRAY** could mean that the provider has mapped a syntax that cannot be mapped to an Automation virtual type.</span></span>

## <a name="examples"></a><span data-ttu-id="f0bd8-129">範例</span><span class="sxs-lookup"><span data-stu-id="f0bd8-129">Examples</span></span>

<span data-ttu-id="f0bd8-130">下列程式碼範例會透過 WinNT 提供者，檢查網路上電腦的 **OperatingSystemVersion** 屬性語法。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-130">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="f0bd8-131">結果語法為字串。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-131">The result syntax is a string.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



<span data-ttu-id="f0bd8-132">下列程式碼範例會透過 WinNT 提供者，檢查網路上電腦的 **OperatingSystemVersion** 屬性語法。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-132">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="f0bd8-133">結果語法為字串。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-133">The result syntax is a string.</span></span> <span data-ttu-id="f0bd8-134">為了簡潔起見，會忽略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="f0bd8-134">For brevity, error checking is omitted.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a><span data-ttu-id="f0bd8-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0bd8-135">Requirements</span></span>



| <span data-ttu-id="f0bd8-136">需求</span><span class="sxs-lookup"><span data-stu-id="f0bd8-136">Requirement</span></span> | <span data-ttu-id="f0bd8-137">值</span><span class="sxs-lookup"><span data-stu-id="f0bd8-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bd8-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0bd8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f0bd8-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0bd8-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0bd8-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0bd8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f0bd8-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0bd8-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0bd8-142">標頭</span><span class="sxs-lookup"><span data-stu-id="f0bd8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0bd8-143"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0bd8-143"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f0bd8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f0bd8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0bd8-145"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0bd8-145"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0bd8-146">IID</span><span class="sxs-lookup"><span data-stu-id="f0bd8-146">IID</span></span><br/>                      | <span data-ttu-id="f0bd8-147">IID \_ IADsSyntax 定義為 C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="f0bd8-147">IID\_IADsSyntax is defined as C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f0bd8-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0bd8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bd8-149">**得到 iadsclass**</span><span class="sxs-lookup"><span data-stu-id="f0bd8-149">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="f0bd8-150">**IADsProperty**</span><span class="sxs-lookup"><span data-stu-id="f0bd8-150">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="f0bd8-151">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="f0bd8-151">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





