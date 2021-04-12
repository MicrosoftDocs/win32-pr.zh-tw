---
title: 'IADsPathname 屬性方法 (Iads .h) '
description: 取得或設定 EscapedMode 屬性。
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- IADsPathname 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187297"
---
# <a name="iadspathname-property-methods"></a><span data-ttu-id="f2768-104">IADsPathname 屬性方法</span><span class="sxs-lookup"><span data-stu-id="f2768-104">IADsPathname Property Methods</span></span>

<span data-ttu-id="f2768-105">[**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)介面的屬性方法會取得或設定 **EscapedMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f2768-105">The property methods of the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface get or set the **EscapedMode** properties.</span></span> <span data-ttu-id="f2768-106">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="f2768-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f2768-107">屬性</span><span class="sxs-lookup"><span data-stu-id="f2768-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f2768-108">**EscapedMode**</span><span class="sxs-lookup"><span data-stu-id="f2768-108">**EscapedMode**</span></span>
<span data-ttu-id="f2768-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f2768-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="f2768-110">檢查或指定在路徑名稱中處理逸出字元的方式。</span><span class="sxs-lookup"><span data-stu-id="f2768-110">Examine or specify how escaped characters are handled in a pathname.</span></span> <span data-ttu-id="f2768-111">如需詳細資訊和定義的選項，請參閱 [**ADS \_ ESCAPE \_ 模式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)。</span><span class="sxs-lookup"><span data-stu-id="f2768-111">For more information and defined options, see [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

<dt>

<span data-ttu-id="f2768-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f2768-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f2768-113">編寫資料類型的腳本： **Long**</span><span class="sxs-lookup"><span data-stu-id="f2768-113">Scripting data type: **Long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="f2768-114">備註</span><span class="sxs-lookup"><span data-stu-id="f2768-114">Remarks</span></span>

<span data-ttu-id="f2768-115">**EscapedMode** 代表狀態。</span><span class="sxs-lookup"><span data-stu-id="f2768-115">**EscapedMode** represents a state.</span></span> <span data-ttu-id="f2768-116">您可以開啟或關閉它，方法是將它設定為 \_ ESCAPEDMODE \_ ON 或 ads \_ ESCAPEDMODE \_ off/ADS \_ ESCAPEDMODE \_ off/ads \_ 的廣告。</span><span class="sxs-lookup"><span data-stu-id="f2768-116">You can turn it on or off, by setting it to ADS\_ESCAPEDMODE\_ON or ADS\_ESCAPEDMODE\_OFF/ADS\_ESCAPEDMODE\_OFF\_EX.</span></span> <span data-ttu-id="f2768-117">開啟或關閉時，所有後續的檢索都會產生轉義或非轉義的路徑字串。</span><span class="sxs-lookup"><span data-stu-id="f2768-117">When it is turned on, or off, all subsequent retrievals produce escaped or unescaped path strings.</span></span>

<span data-ttu-id="f2768-118">在 ADSI 中，只有 [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) 能夠未逸出路徑。</span><span class="sxs-lookup"><span data-stu-id="f2768-118">In ADSI only the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) is capable of unescaping paths.</span></span> <span data-ttu-id="f2768-119">所有其他 ADSI 介面一律會傳回已轉義的路徑。</span><span class="sxs-lookup"><span data-stu-id="f2768-119">All other ADSI interfaces always return escaped paths.</span></span> <span data-ttu-id="f2768-120">**EscapedMode** 的預設狀態是 ads \_ EscapedMode \_ 預設值，如 [**ads \_ ESCAPE \_ 模式 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)中所定義。</span><span class="sxs-lookup"><span data-stu-id="f2768-120">The default state of **EscapedMode** is ADS\_ESCAPEDMODE\_DEFAULT as defined in [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

## <a name="examples"></a><span data-ttu-id="f2768-121">範例</span><span class="sxs-lookup"><span data-stu-id="f2768-121">Examples</span></span>

<span data-ttu-id="f2768-122">下列程式碼範例示範如何使用 **EscapedMode** 屬性，將下列三個特殊字元的轉換開啟/關閉： "="、"、" 和 "/"。</span><span class="sxs-lookup"><span data-stu-id="f2768-122">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



<span data-ttu-id="f2768-123">下列程式碼範例示範如何使用 **EscapedMode** 屬性，將下列三個特殊字元的轉換開啟/關閉： "="、"、" 和 "/"。</span><span class="sxs-lookup"><span data-stu-id="f2768-123">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



<span data-ttu-id="f2768-124">下列程式碼範例顯示如何使用 **EscapedMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f2768-124">The following code example shows how to work with the **EscapedMode** property.</span></span> <span data-ttu-id="f2768-125">忽略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="f2768-125">Error checking is ignored.</span></span>


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a><span data-ttu-id="f2768-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2768-126">Requirements</span></span>



| <span data-ttu-id="f2768-127">需求</span><span class="sxs-lookup"><span data-stu-id="f2768-127">Requirement</span></span> | <span data-ttu-id="f2768-128">值</span><span class="sxs-lookup"><span data-stu-id="f2768-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2768-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2768-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2768-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2768-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2768-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2768-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2768-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2768-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2768-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f2768-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2768-134"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2768-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f2768-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f2768-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2768-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2768-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2768-137">IID</span><span class="sxs-lookup"><span data-stu-id="f2768-137">IID</span></span><br/>                      | <span data-ttu-id="f2768-138">IID \_ IADsPathname 定義為 D592AED4-F420-11D0-A36E-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="f2768-138">IID\_IADsPathname is defined as D592AED4-F420-11D0-A36E-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="f2768-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2768-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2768-140">**IADsPathname**</span><span class="sxs-lookup"><span data-stu-id="f2768-140">**IADsPathname**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[<span data-ttu-id="f2768-141">**ADS \_ ESCAPE \_ 模式 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="f2768-141">**ADS\_ESCAPE\_MODE\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





