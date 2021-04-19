---
title: 'IADsWinNTSystemInfo 屬性方法 (Iads .h) '
description: IADsWinNTSystemInfo 介面的屬性方法會取得或設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- IADsWinNTSystemInfo 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966289"
---
# <a name="iadswinntsysteminfo-property-methods"></a><span data-ttu-id="5d74d-105">IADsWinNTSystemInfo 屬性方法</span><span class="sxs-lookup"><span data-stu-id="5d74d-105">IADsWinNTSystemInfo Property Methods</span></span>

<span data-ttu-id="5d74d-106">[**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)介面的屬性方法會取得或設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="5d74d-106">The property methods of the [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="5d74d-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="5d74d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5d74d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="5d74d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5d74d-109">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="5d74d-109">**ComputerName**</span></span>
<span data-ttu-id="5d74d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5d74d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5d74d-111">正在執行應用程式的主電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="5d74d-111">Name of the host computer where the application is running.</span></span>

<dt>

<span data-ttu-id="5d74d-112">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d74d-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d74d-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5d74d-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d74d-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="5d74d-114">**DomainName**</span></span>
<span data-ttu-id="5d74d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5d74d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5d74d-116">使用者所屬之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d74d-116">Name of the domain to which the user belongs.</span></span>

<dt>

<span data-ttu-id="5d74d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d74d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d74d-118">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5d74d-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d74d-119">**Pdc**</span><span class="sxs-lookup"><span data-stu-id="5d74d-119">**PDC**</span></span>
<span data-ttu-id="5d74d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5d74d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="5d74d-121">主機電腦所屬之網域主控站的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d74d-121">Name of the primary domain controller to which the host computer belongs.</span></span>

<dt>

<span data-ttu-id="5d74d-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d74d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d74d-123">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5d74d-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d74d-124">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="5d74d-124">**UserName**</span></span>
<span data-ttu-id="5d74d-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5d74d-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="5d74d-126">建立 **WinNTSystemInfo** 物件時所使用之使用者帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d74d-126">Name of the user account under which the **WinNTSystemInfo** object is created.</span></span>

<dt>

<span data-ttu-id="5d74d-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d74d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d74d-128">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5d74d-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="5d74d-129">範例</span><span class="sxs-lookup"><span data-stu-id="5d74d-129">Examples</span></span>

<span data-ttu-id="5d74d-130">下列 C/c + + 程式碼範例會捕獲 WinNT 系統資訊。</span><span class="sxs-lookup"><span data-stu-id="5d74d-130">The following C/C++ code example retrieves the WinNT system information.</span></span> <span data-ttu-id="5d74d-131">為了簡潔起見，會忽略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="5d74d-131">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="5d74d-132">下列 Visual Basic 程式碼範例會捕獲 WinNT 系統資訊。</span><span class="sxs-lookup"><span data-stu-id="5d74d-132">The following Visual Basic code example retrieves the WinNT system information.</span></span>


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



<span data-ttu-id="5d74d-133">下列 Visual Basic Scripting Edition/Active Server Pages 程式碼範例會抓取 WinNT 系統資訊。</span><span class="sxs-lookup"><span data-stu-id="5d74d-133">The following Visual Basic Scripting Edition/Active Server Pages code example retrieves the WinNT system information.</span></span>


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a><span data-ttu-id="5d74d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d74d-134">Requirements</span></span>



| <span data-ttu-id="5d74d-135">需求</span><span class="sxs-lookup"><span data-stu-id="5d74d-135">Requirement</span></span> | <span data-ttu-id="5d74d-136">值</span><span class="sxs-lookup"><span data-stu-id="5d74d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d74d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d74d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5d74d-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d74d-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d74d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d74d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5d74d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d74d-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d74d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="5d74d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d74d-142"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d74d-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5d74d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5d74d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d74d-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d74d-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d74d-145">IID</span><span class="sxs-lookup"><span data-stu-id="5d74d-145">IID</span></span><br/>                      | <span data-ttu-id="5d74d-146">IID \_ IADsWinNTSystemInfo 定義為6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="5d74d-146">IID\_IADsWinNTSystemInfo is defined as 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5d74d-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d74d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d74d-148">**IADsWinNTSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="5d74d-148">**IADsWinNTSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





