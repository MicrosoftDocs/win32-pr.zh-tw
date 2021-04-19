---
description: 在元件的資訊清單中，抓取與指定 GUID 相關聯的類別名稱和其他資訊。
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983998"
---
# <a name="sxslookupclrguid-function"></a><span data-ttu-id="7501b-103">SxsLookupClrGuid 函式</span><span class="sxs-lookup"><span data-stu-id="7501b-103">SxsLookupClrGuid function</span></span>

<span data-ttu-id="7501b-104">在元件的資訊清單中，抓取與指定 GUID 相關聯的類別名稱和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7501b-104">Retrieves the class name and other information associated with a given GUID in a component's manifest.</span></span> <span data-ttu-id="7501b-105">只有在 .NET Framework 中執行低層級的 managed 非受控互通性時，才會使用此函數。</span><span class="sxs-lookup"><span data-stu-id="7501b-105">This function is used only when implementing low-level managed-unmanaged interoperability in the .NET Framework.</span></span> <span data-ttu-id="7501b-106">如需受管理的非受控互通性的詳細資訊，請參閱 .NET Framework SDK 以及 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)中的「與非受控碼互通」。</span><span class="sxs-lookup"><span data-stu-id="7501b-106">For more information about managed-unmanaged interoperability, see "Interoperating with Unmanaged Code" in the .NET Framework SDK and also [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7501b-107">語法</span><span class="sxs-lookup"><span data-stu-id="7501b-107">Syntax</span></span>


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="7501b-108">參數</span><span class="sxs-lookup"><span data-stu-id="7501b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7501b-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7501b-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7501b-110">零或多個下列旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="7501b-110">A combination of zero or more of the following flags.</span></span>



| <span data-ttu-id="7501b-111">值</span><span class="sxs-lookup"><span data-stu-id="7501b-111">Value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="7501b-112">意義</span><span class="sxs-lookup"><span data-stu-id="7501b-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <span data-ttu-id="7501b-113"><dt>**SXS \_查閱 \_ CLR \_ GUID \_ 使用 \_ ACTCTX**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7501b-113"><dt>**SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX**</dt> <dt>0x00000001</dt></span></span> </dl>              | <span data-ttu-id="7501b-114">如果設定此旗標，則 *hActCtx* 參數必須包含 [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) 函數所傳回的啟用內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="7501b-114">If this flag is set, then the *hActCtx* parameter must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="7501b-115">如果未設定此旗標，則會忽略 *hActCtx* 參數，而 **SxsLookupClrGuid** 會搜尋目前作用中的啟用內容 (使用 [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) 函式來讓啟用內容變成作用中) 。</span><span class="sxs-lookup"><span data-stu-id="7501b-115">If this flag is not set, the *hActCtx* parameter is ignored and **SxsLookupClrGuid** searches the activation context that is currently active (the [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) function is used to make an activation context active).</span></span><br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <span data-ttu-id="7501b-116"><dt>**SXS \_查閱 \_ CLR \_ GUID \_ 尋找 \_ 代理**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="7501b-116"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE**</dt> <dt>0x00010000</dt></span></span> </dl>  | <span data-ttu-id="7501b-117">如果設定此旗標， **SxsLookupClrGuid** 會搜尋是否有代理。</span><span class="sxs-lookup"><span data-stu-id="7501b-117">If this flag is set, **SxsLookupClrGuid** searches for a surrogate.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <span data-ttu-id="7501b-118"><dt>**SXS \_查閱 \_ clr \_ GUID \_ 尋找 \_ clr \_ 類別**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="7501b-118"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="7501b-119">如果設定此旗標， **SxsLookupClrGuid** 會搜尋類別。</span><span class="sxs-lookup"><span data-stu-id="7501b-119">If this flag is set, **SxsLookupClrGuid** searches for a class.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <span data-ttu-id="7501b-120"><dt>**SXS \_查閱 \_ CLR \_ GUID \_ 尋找 \_ 任何**</dt> <dt>0x00030000</dt></span><span class="sxs-lookup"><span data-stu-id="7501b-120"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_ANY**</dt> <dt>0x00030000</dt></span></span> </dl>                    | <span data-ttu-id="7501b-121">這是 **SXS \_ lookup \_ clr \_ Guid \_ find \_ 代理** 和 **SXS \_ lookup \_ clr \_ guid \_ find \_ Clr \_ 類別** 旗標的組合; 如果兩者都已設定， **SxsLookupClrGuid** 就會先搜尋代理，並在找不到它時搜尋某個類別。</span><span class="sxs-lookup"><span data-stu-id="7501b-121">This is a combination of the **SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE** and **SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS** flags; if both are set, **SxsLookupClrGuid** searches for a surrogate first, and only if it does not find one, then searches for a class.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="7501b-122">*pClsid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7501b-122">*pClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7501b-123">指標，指向要在其上搜尋交互操作資訊之啟用內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7501b-123">A pointer to the GUID about which to search the activation context for interoperation information.</span></span> <span data-ttu-id="7501b-124">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7501b-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7501b-125">*hActCtx* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7501b-125">*hActCtx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7501b-126">如果在 *dwFlags* 參數中設定 **SXS \_ LOOKUP \_ CLR \_ GUID \_ USE \_ ACTCTX** 旗標，則 *hActCtx* 必須包含 [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)函式所傳回的啟用內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="7501b-126">If the **SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX** flag is set in the *dwFlags* parameter, then *hActCtx* must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="7501b-127">否則會忽略 *hActCtx* 。</span><span class="sxs-lookup"><span data-stu-id="7501b-127">Otherwise, *hActCtx* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="7501b-128">*pvOutputBuffer* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="7501b-128">*pvOutputBuffer* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7501b-129">要在其中複製傳回信息的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="7501b-129">Pointer to the buffer into which return information is copied.</span></span> <span data-ttu-id="7501b-130">只有當 *cbOutputBuffer* 參數為零值時，此參數才可以是 Null 值。</span><span class="sxs-lookup"><span data-stu-id="7501b-130">This parameter may be NULL-valued only if the *cbOutputBuffer* parameter is zero-valued.</span></span> <span data-ttu-id="7501b-131">如果有任何) 包含 **SXS \_ GUID \_ 資訊 \_ CLR** 結構，後面接著所需的任何其他字串資料，則會將資料放在這個緩衝區的結束 (。</span><span class="sxs-lookup"><span data-stu-id="7501b-131">The data placed in this buffer on exit (if any) consists of a **SXS\_GUID\_INFORMATION\_CLR** structure followed by any additional string data required.</span></span> <span data-ttu-id="7501b-132">如需詳細資訊，請參閱下面的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="7501b-132">See the Remarks section below for more information.</span></span>

</dd> <dt>

<span data-ttu-id="7501b-133">*cbOutputBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7501b-133">*cbOutputBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7501b-134">*PvOutputBuffer* 參數所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7501b-134">Size in bytes of the buffer pointed to by the *pvOutputBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7501b-135">*pcbOutputBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7501b-135">*pcbOutputBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7501b-136">變數的指標，此變數會在結束時放置傳回信息的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7501b-136">Pointer to a variable where the size, in bytes, of the return information is placed on exit.</span></span> <span data-ttu-id="7501b-137">如果 *cbOutputBuffer* 參數為零，或如果輸出緩衝區的大小小於傳回信息的大小，則 **SxsLookupClrGuid** 會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 **\_ \_ 緩衝區不足** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7501b-137">If the *cbOutputBuffer* parameter is zero, or if the size of the output buffer is smaller than the size of the return information, then **SxsLookupClrGuid** fails and [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns an error of **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="7501b-138">在這種情況下，請使用 *pcbOutputBuffer* 所指向之變數中的值來配置夠大的緩衝區，然後再次呼叫 **SxsLookupClrGuid** 來取出所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7501b-138">In this case, use the value in the variable pointed to by *pcbOutputBuffer* to allocate a large enough buffer, and then call **SxsLookupClrGuid** again to retrieve the desired information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7501b-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="7501b-139">Return value</span></span>

<span data-ttu-id="7501b-140">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7501b-140">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="7501b-141">如需詳細的錯誤資訊，請呼叫 [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="7501b-141">For more error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>

## <a name="remarks"></a><span data-ttu-id="7501b-142">備註</span><span class="sxs-lookup"><span data-stu-id="7501b-142">Remarks</span></span>

<span data-ttu-id="7501b-143">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="7501b-143">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="7501b-144">Managed 元件可能會將本身宣告為支援 managed 「interop 元件」，以便讓未受管理的 Win32 元件取用者參考宣告元件。</span><span class="sxs-lookup"><span data-stu-id="7501b-144">Managed components may declare themselves as supporting managed "interop assemblies" so as to allow an unmanaged Win32 component consumer to reference the declaring assembly.</span></span> <span data-ttu-id="7501b-145">元件取用者可以在 GUID 上呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以與受控元件互動。</span><span class="sxs-lookup"><span data-stu-id="7501b-145">The component consumer can interact with the managed component by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on a GUID.</span></span> <span data-ttu-id="7501b-146">交互操作層會將物件建立要求路由至 .NET Framework、建立 managed 物件的實例，並傳回介面指標。</span><span class="sxs-lookup"><span data-stu-id="7501b-146">The interoperation layer routes the object creation request to .NET Framework, creates an instance of the managed object, and returns an interface pointer.</span></span>

<span data-ttu-id="7501b-147">**SxsLookupClrGuid** 可讓架構在元件的資訊清單中，取得與指定 GUID 相關聯的資訊，例如其 .net 類別名稱、所需的 .NET Framework 版本，以及它所在的主機元件。</span><span class="sxs-lookup"><span data-stu-id="7501b-147">**SxsLookupClrGuid** allows the frameworks to retrieve information associated with a given GUID in the component's manifest, such as what its .NET class name is, what version of the .NET Framework it requires, and what host assembly it is located in.</span></span> <span data-ttu-id="7501b-148">Managed 元件會發行包含一些語句的 interop 元件，該元件會將 Guid 與元件和類型名稱建立關聯，而 .NET 執行時間會在呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 時，將 managed 物件實例的結構代理程式代理程式。</span><span class="sxs-lookup"><span data-stu-id="7501b-148">Managed components publish an interop assembly that contains a number of statements associating GUIDs with assembly and type names, and the .NET runtime brokers the construction of managed object instances when [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is called.</span></span>

<span data-ttu-id="7501b-149">以下是宣告 CLR GUID 的範例元件資訊清單，以及 **SxsLookupClrGuid** 可以查詢的 clr 代理：</span><span class="sxs-lookup"><span data-stu-id="7501b-149">The following is a sample component manifest declaring a CLR GUID and a CLR surrogate that **SxsLookupClrGuid** can look up:</span></span>

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

<span data-ttu-id="7501b-150">互通性提供者會使用 GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" 的指標來呼叫 **SxsLookupClrGuid** ，而且會在中傳回類別名稱 "MySampleSurrogate"、所需的執行階段版本 "1.0.3055"，以及主控元件的文字識別 "DotNet"、version = ' 1.0.0.0 '、type = ' interop ' "。</span><span class="sxs-lookup"><span data-stu-id="7501b-150">An interoperation provider would call **SxsLookupClrGuid** with a pointer to the GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", and would receive in return the class name "MySampleSurrogate", the required runtime version "1.0.3055", and the textual identity "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" of the hosting component.</span></span>

<span data-ttu-id="7501b-151">這項傳回信息會包含及/或由如下所宣告的 **SXS \_ GUID \_ 資訊 \_ CLR** 結構參考。</span><span class="sxs-lookup"><span data-stu-id="7501b-151">This return information would be contained and/or referenced by a **SXS\_GUID\_INFORMATION\_CLR** structure declared as follows.</span></span>

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

<span data-ttu-id="7501b-152">此結構的成員包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="7501b-152">The members of this structure contain the following information.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7501b-153">member</span><span class="sxs-lookup"><span data-stu-id="7501b-153">Member</span></span></th>
<th><span data-ttu-id="7501b-154">描述</span><span class="sxs-lookup"><span data-stu-id="7501b-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7501b-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span><span class="sxs-lookup"><span data-stu-id="7501b-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span></span><br/></td>
<td><span data-ttu-id="7501b-156">包含 SXS_GUID_INFORMATION_CLR 結構的大小， (這可讓結構在較新的版本) 中成長。</span><span class="sxs-lookup"><span data-stu-id="7501b-156">Contains the size of the SXS_GUID_INFORMATION_CLR structure (this allows the structure to grow in later versions).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7501b-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span><span class="sxs-lookup"><span data-stu-id="7501b-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span></span><br/></td>
<td><span data-ttu-id="7501b-158">包含下列兩個旗標值的其中一個：</span><span class="sxs-lookup"><span data-stu-id="7501b-158">Contains one of the following two flag values:</span></span> <br/>
<ul>
<li><span data-ttu-id="7501b-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001) ：表示指定的 GUID 與代理相關聯 &quot; 。&quot;</span><span class="sxs-lookup"><span data-stu-id="7501b-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Indicates that the specified GUID was associated with a &quot;surrogate.&quot;</span></span></li>
<li><span data-ttu-id="7501b-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002) ：表示指定的 GUID 與類別相關聯 &quot; 。&quot;</span><span class="sxs-lookup"><span data-stu-id="7501b-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Indicates that the specified GUID was associated with a &quot;class.&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7501b-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span><span class="sxs-lookup"><span data-stu-id="7501b-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span></span><br/></td>
<td><span data-ttu-id="7501b-162">指向以零結尾的寬字元字串，識別此類別的主機資訊清單中指定的執行階段版本。</span><span class="sxs-lookup"><span data-stu-id="7501b-162">Points to a zero-terminated wide-character string that identifies the version of the runtime specified in the host manifest for this class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7501b-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="7501b-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span></span><br/></td>
<td><span data-ttu-id="7501b-164">指向以零結尾的寬字元字串，其中包含與指定 GUID 相關聯的 .NET 類別名稱。</span><span class="sxs-lookup"><span data-stu-id="7501b-164">Points to a zero-terminated wide-character string that contains the name of the .NET class associated with the specified GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7501b-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="7501b-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span></span><br/></td>
<td><span data-ttu-id="7501b-166">指向以零結尾的寬字元字串，其中包含裝載這個類別之元件的文字識別。</span><span class="sxs-lookup"><span data-stu-id="7501b-166">Points to a zero-terminated wide-character string that contains the textual identity of the assembly that hosts this class.</span></span> <span data-ttu-id="7501b-167">如需文字身分識別的詳細資訊，請參閱在 &quot; &quot; &quot; 執行時間 &quot; &quot; 使用 .NET Framework SDK 中的 .NET Framework，在 [在執行時間探索類型資訊] 下指定完整的類型名稱 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7501b-167">For more information about textual identity, see &quot;Specifying Fully Qualified Type Names&quot; under &quot;Discovering Type Information at Run Time&quot; under &quot;Programming with the .NET Framework&quot; in the .NET Framework SDK.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7501b-168">未受管理的應用程式可以使用以這種方式傳回的資訊來載入正確版本的 .NET Framework、載入 **pcwszAssemblyIdentity** 元素所識別的元件，然後建立 **pcwszTypeName** 專案所命名的類別實例。</span><span class="sxs-lookup"><span data-stu-id="7501b-168">An unmanaged application can use the information returned in this fashion to load the right version of the .NET Framework, load the assembly identified by the **pcwszAssemblyIdentity** element, and then create an instance of the class named by the **pcwszTypeName** element.</span></span>

## <a name="examples"></a><span data-ttu-id="7501b-169">範例</span><span class="sxs-lookup"><span data-stu-id="7501b-169">Examples</span></span>

<span data-ttu-id="7501b-170">使用動態連結，如下所示呼叫 **SxsLookupClrGuid** 函數：</span><span class="sxs-lookup"><span data-stu-id="7501b-170">Use dynamic linking as follows to call the **SxsLookupClrGuid** function:</span></span>


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a><span data-ttu-id="7501b-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="7501b-171">Requirements</span></span>



| <span data-ttu-id="7501b-172">需求</span><span class="sxs-lookup"><span data-stu-id="7501b-172">Requirement</span></span> | <span data-ttu-id="7501b-173">值</span><span class="sxs-lookup"><span data-stu-id="7501b-173">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7501b-174">DLL</span><span class="sxs-lookup"><span data-stu-id="7501b-174">DLL</span></span><br/> | <dl> <span data-ttu-id="7501b-175"><dt>Mscoree.dll;</dt><dt>Sxs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7501b-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7501b-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7501b-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7501b-177">隔離應用程式和並存組件</span><span class="sxs-lookup"><span data-stu-id="7501b-177">Isolated Applications and Side-by-side Assemblies</span></span>](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[<span data-ttu-id="7501b-178">**CreateActCtx**</span><span class="sxs-lookup"><span data-stu-id="7501b-178">**CreateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[<span data-ttu-id="7501b-179">**ActivateActCtx**</span><span class="sxs-lookup"><span data-stu-id="7501b-179">**ActivateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[<span data-ttu-id="7501b-180">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="7501b-180">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
