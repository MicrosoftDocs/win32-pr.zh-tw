---
title: 'IADsADSystemInfo 屬性方法 (Iads .h) '
description: IADsADSystemInfo 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- IADsADSystemInfo 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105167"
---
# <a name="iadsadsysteminfo-property-methods"></a><span data-ttu-id="f1e8d-105">IADsADSystemInfo 屬性方法</span><span class="sxs-lookup"><span data-stu-id="f1e8d-105">IADsADSystemInfo Property Methods</span></span>

<span data-ttu-id="f1e8d-106">[**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-106">The property methods of the [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="f1e8d-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f1e8d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f1e8d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f1e8d-109">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-109">**ComputerName**</span></span>
<span data-ttu-id="f1e8d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-111">抓取本機電腦的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-111">Retrieves the distinguished name of the local computer.</span></span>

<dt>

<span data-ttu-id="f1e8d-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-114">**DomainDNSName**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-114">**DomainDNSName**</span></span>
<span data-ttu-id="f1e8d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-116">抓取本機電腦網域的 DNS 名稱，例如 "domainName.companyName.com"。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-116">Retrieves the DNS name of the local computer's domain, such as "domainName.companyName.com".</span></span>

<dt>

<span data-ttu-id="f1e8d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-119">**DomainShortName**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-119">**DomainShortName**</span></span>
<span data-ttu-id="f1e8d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-121">抓取本機電腦網域的簡短名稱，例如 "domainName"。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-121">Retrieves the short name of the local computer's domain, such as "domainName".</span></span>

<dt>

<span data-ttu-id="f1e8d-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-124">**ForestDNSName**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-124">**ForestDNSName**</span></span>
<span data-ttu-id="f1e8d-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-126">抓取本機電腦樹系的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-126">Retrieves the DNS name of the local computer's forest.</span></span>

<dt>

<span data-ttu-id="f1e8d-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-128">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-129">**IsNativeMode**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-129">**IsNativeMode**</span></span>
<span data-ttu-id="f1e8d-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-131">判斷本機電腦的網域是否為原生或混合模式。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-131">Determines whether the local computer's domain is in native or mixed mode.</span></span>

<dt>

<span data-ttu-id="f1e8d-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-133">編寫資料類型的腳本： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-133">Scripting data type: **BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-134">**PDCRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-134">**PDCRoleOwner**</span></span>
<span data-ttu-id="f1e8d-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-136">針對擁有本機電腦網域中網域主控站角色的 DC，抓取目錄服務代理程式 (DSA) 物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-136">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the primary domain controller role in the local computer's domain.</span></span>

<dt>

<span data-ttu-id="f1e8d-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-138">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-139">**SchemaRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-139">**SchemaRoleOwner**</span></span>
<span data-ttu-id="f1e8d-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-141">針對在本機電腦樹系中擁有架構主機角色的 DC，抓取目錄服務代理程式 (DSA) 物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-141">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the schema master role in the local computer's forest.</span></span>

<dt>

<span data-ttu-id="f1e8d-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-143">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-144">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-144">**SiteName**</span></span>
<span data-ttu-id="f1e8d-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-146">抓取本機電腦的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-146">Retrieves the site name of the local computer.</span></span>

<dt>

<span data-ttu-id="f1e8d-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-148">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-148">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f1e8d-149">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-149">**UserName**</span></span>
<span data-ttu-id="f1e8d-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f1e8d-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="f1e8d-151">抓取目前使用者的 Active Directory 辨別名稱，也就是已登入的使用者或呼叫端執行緒所模擬的使用者。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-151">Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.</span></span>

<dt>

<span data-ttu-id="f1e8d-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1e8d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1e8d-153">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-153">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="f1e8d-154">範例</span><span class="sxs-lookup"><span data-stu-id="f1e8d-154">Examples</span></span>

<span data-ttu-id="f1e8d-155">下列 c + + 程式碼範例會捕獲 Windows 系統資訊。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-155">The following C++ code example retrieves the Windows system information.</span></span> <span data-ttu-id="f1e8d-156">為了簡潔起見，會忽略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-156">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="f1e8d-157">下列 Visual Basic 程式碼範例會捕獲 Windows 系統資訊。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-157">The following Visual Basic code example retrieves the Windows system information.</span></span>


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



<span data-ttu-id="f1e8d-158">下列 VBScript/ASP 程式碼範例會捕獲 Windows 系統資訊。</span><span class="sxs-lookup"><span data-stu-id="f1e8d-158">The following VBScript/ASP code example retrieves the Windows system information.</span></span>


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a><span data-ttu-id="f1e8d-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1e8d-159">Requirements</span></span>



| <span data-ttu-id="f1e8d-160">需求</span><span class="sxs-lookup"><span data-stu-id="f1e8d-160">Requirement</span></span> | <span data-ttu-id="f1e8d-161">值</span><span class="sxs-lookup"><span data-stu-id="f1e8d-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e8d-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1e8d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e8d-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1e8d-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1e8d-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1e8d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e8d-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1e8d-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1e8d-166">標頭</span><span class="sxs-lookup"><span data-stu-id="f1e8d-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e8d-167"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e8d-167"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f1e8d-168">DLL</span><span class="sxs-lookup"><span data-stu-id="f1e8d-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1e8d-169"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1e8d-169"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f1e8d-170">IID</span><span class="sxs-lookup"><span data-stu-id="f1e8d-170">IID</span></span><br/>                      | <span data-ttu-id="f1e8d-171">IID \_ IADsADSystemInfo 定義為5BB11929-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="f1e8d-171">IID\_IADsADSystemInfo is defined as 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="f1e8d-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1e8d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e8d-173">**IADsADSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-173">**IADsADSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[<span data-ttu-id="f1e8d-174">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="f1e8d-174">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

