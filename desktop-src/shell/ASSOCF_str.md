---
description: 提供 IQueryAssociations 介面方法的資訊。
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: ASSOCF 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195789"
---
# <a name="assocf-enumeration"></a><span data-ttu-id="ca94a-103">ASSOCF 列舉</span><span class="sxs-lookup"><span data-stu-id="ca94a-103">ASSOCF enumeration</span></span>

<span data-ttu-id="ca94a-104">提供 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 介面方法的資訊。</span><span class="sxs-lookup"><span data-stu-id="ca94a-104">Provides information to the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca94a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca94a-105">Syntax</span></span>

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="ca94a-106">C++</span><span class="sxs-lookup"><span data-stu-id="ca94a-106">C++</span></span></th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a><span data-ttu-id="ca94a-107">常數</span><span class="sxs-lookup"><span data-stu-id="ca94a-107">Constants</span></span>

 <span data-ttu-id="ca94a-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ 無**</span><span class="sxs-lookup"><span data-stu-id="ca94a-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF\_NONE**</span></span> 

<span data-ttu-id="ca94a-109">未設定下列任何選項。</span><span class="sxs-lookup"><span data-stu-id="ca94a-109">None of the following options are set.</span></span>

 <span data-ttu-id="ca94a-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ INIT \_ NOREMAPCLSID**</span><span class="sxs-lookup"><span data-stu-id="ca94a-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF\_INIT\_NOREMAPCLSID**</span></span> 

<span data-ttu-id="ca94a-111">指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 介面方法不要將 CLSID 值對應至 ProgID 值。</span><span class="sxs-lookup"><span data-stu-id="ca94a-111">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods not to map CLSID values to ProgID values.</span></span>

 <span data-ttu-id="ca94a-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ INIT \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="ca94a-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF\_INIT\_BYEXENAME**</span></span> 

<span data-ttu-id="ca94a-113">識別 [**IQueryAssociations：： Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init)的 *pwszAssoc* 參數值，做為可執行檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ca94a-113">Identifies the value of the *pwszAssoc* parameter of [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) as an executable file name.</span></span> <span data-ttu-id="ca94a-114">如果未設定此旗標，則會將根機碼設定為與 **.exe** 索引鍵相關聯的 progid，而不是可執行檔的 progid。</span><span class="sxs-lookup"><span data-stu-id="ca94a-114">If this flag is not set, the root key will be set to the ProgID associated with the **.exe** key instead of the executable file's ProgID.</span></span>

 <span data-ttu-id="ca94a-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ 開啟 \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="ca94a-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF\_OPEN\_BYEXENAME**</span></span> 

<span data-ttu-id="ca94a-116">與 **ASSOCF \_ INIT \_ BYEXENAME** 相同。</span><span class="sxs-lookup"><span data-stu-id="ca94a-116">Identical to **ASSOCF\_INIT\_BYEXENAME**.</span></span>

 <span data-ttu-id="ca94a-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ INIT \_ DEFAULTTOSTAR**</span><span class="sxs-lookup"><span data-stu-id="ca94a-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF\_INIT\_DEFAULTTOSTAR**</span></span> 

<span data-ttu-id="ca94a-118">指定當 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法在根機碼下找不到要求的值時，應該嘗試從子機碼取得可比較的值 **\*** 。</span><span class="sxs-lookup"><span data-stu-id="ca94a-118">Specifies that when an [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **\*** subkey.</span></span>

 <span data-ttu-id="ca94a-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ INIT \_ DEFAULTTOFOLDER**</span><span class="sxs-lookup"><span data-stu-id="ca94a-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF\_INIT\_DEFAULTTOFOLDER**</span></span> 

<span data-ttu-id="ca94a-120">指定當 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法在根機碼下找不到要求的值時，應該嘗試從 **資料夾** 子機碼取得可比較的值。</span><span class="sxs-lookup"><span data-stu-id="ca94a-120">Specifies that when a [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **Folder** subkey.</span></span>

 <span data-ttu-id="ca94a-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="ca94a-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF\_NOUSERSETTINGS**</span></span> 

<span data-ttu-id="ca94a-122">指定只搜尋 **HKEY \_ 類別 \_ 根目錄** ，且應忽略 HKEY 的 **\_ 目前 \_ 使用者** 。</span><span class="sxs-lookup"><span data-stu-id="ca94a-122">Specifies that only **HKEY\_CLASSES\_ROOT** should be searched, and that **HKEY\_CURRENT\_USER** should be ignored.</span></span>

 <span data-ttu-id="ca94a-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="ca94a-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF\_NOTRUNCATE**</span></span> 

<span data-ttu-id="ca94a-124">指定不應該截斷傳回字串。</span><span class="sxs-lookup"><span data-stu-id="ca94a-124">Specifies that the return string should not be truncated.</span></span> <span data-ttu-id="ca94a-125">相反地，會傳回錯誤值和完整字串所需的大小。</span><span class="sxs-lookup"><span data-stu-id="ca94a-125">Instead, return an error value and the required size for the complete string.</span></span>

 <span data-ttu-id="ca94a-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ 確認**</span><span class="sxs-lookup"><span data-stu-id="ca94a-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF\_VERIFY**</span></span> 

<span data-ttu-id="ca94a-127">指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法驗證資料是否正確。</span><span class="sxs-lookup"><span data-stu-id="ca94a-127">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to verify that data is accurate.</span></span> <span data-ttu-id="ca94a-128">此設定可讓 **IQueryAssociations** 方法從使用者的硬碟讀取資料以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ca94a-128">This setting allows **IQueryAssociations** methods to read data from the user's hard disk for verification.</span></span> <span data-ttu-id="ca94a-129">例如，他們可以在登錄中檢查儲存在 .exe 檔案中的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="ca94a-129">For example, they can check the friendly name in the registry against the one stored in the .exe file.</span></span> <span data-ttu-id="ca94a-130">設定此旗標通常可減少方法的效率。</span><span class="sxs-lookup"><span data-stu-id="ca94a-130">Setting this flag typically reduces the efficiency of the method.</span></span>

 <span data-ttu-id="ca94a-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL**</span><span class="sxs-lookup"><span data-stu-id="ca94a-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF\_REMAPRUNDLL**</span></span> 

<span data-ttu-id="ca94a-132">指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法略過 Rundll.exe，並傳回其目標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca94a-132">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to ignore Rundll.exe and return information about its target.</span></span> <span data-ttu-id="ca94a-133">通常 **IQueryAssociations** 方法會傳回命令字串中的第一個 .exe 或 .dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca94a-133">Typically **IQueryAssociations** methods return information about the first .exe or .dll in a command string.</span></span> <span data-ttu-id="ca94a-134">如果命令使用 Rundll.exe，設定這個旗標會告知方法忽略 Rundll.exe 並傳回其目標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca94a-134">If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.</span></span>

 <span data-ttu-id="ca94a-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOFIXUPS**</span><span class="sxs-lookup"><span data-stu-id="ca94a-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF\_NOFIXUPS**</span></span> 

<span data-ttu-id="ca94a-136">指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法不要修正登錄中的錯誤，例如函式的易記名稱與 .exe 檔案中找到的函式不相符。</span><span class="sxs-lookup"><span data-stu-id="ca94a-136">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.</span></span>

 <span data-ttu-id="ca94a-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS**</span><span class="sxs-lookup"><span data-stu-id="ca94a-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF\_IGNOREBASECLASS**</span></span> 

<span data-ttu-id="ca94a-138">指定應該忽略 BaseClass 值。</span><span class="sxs-lookup"><span data-stu-id="ca94a-138">Specifies that the BaseClass value should be ignored.</span></span>

 <span data-ttu-id="ca94a-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ INIT \_ IGNOREUNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ca94a-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF\_INIT\_IGNOREUNKNOWN**</span></span> 

<span data-ttu-id="ca94a-140">**在 Windows 7 中引進**。</span><span class="sxs-lookup"><span data-stu-id="ca94a-140">**Introduced in Windows 7**.</span></span> <span data-ttu-id="ca94a-141">指定應忽略「未知」 ProgID;相反地，會失敗。</span><span class="sxs-lookup"><span data-stu-id="ca94a-141">Specifies that the "Unknown" ProgID should be ignored; instead, fail.</span></span>

 <span data-ttu-id="ca94a-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ INIT \_ FIXED \_ PROGID**</span><span class="sxs-lookup"><span data-stu-id="ca94a-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF\_INIT\_FIXED\_PROGID**</span></span> 

<span data-ttu-id="ca94a-143">**Windows 8 引進**。</span><span class="sxs-lookup"><span data-stu-id="ca94a-143">**Introduced in Windows 8**.</span></span> <span data-ttu-id="ca94a-144">指定提供的 ProgID 應使用系統預設值進行對應，而不是目前的使用者預設值。</span><span class="sxs-lookup"><span data-stu-id="ca94a-144">Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.</span></span>

 <span data-ttu-id="ca94a-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ 是 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="ca94a-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF\_IS\_PROTOCOL**</span></span> 

<span data-ttu-id="ca94a-146">**Windows 8 引進**。</span><span class="sxs-lookup"><span data-stu-id="ca94a-146">**Introduced in Windows 8**.</span></span> <span data-ttu-id="ca94a-147">指定值為通訊協定，且應使用目前的使用者預設值進行對應。</span><span class="sxs-lookup"><span data-stu-id="ca94a-147">Specifies that the value is a protocol, and should be mapped using the current user defaults.</span></span>

 <span data-ttu-id="ca94a-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ INIT \_ FOR \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="ca94a-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF\_INIT\_FOR\_FILE**</span></span> 

<span data-ttu-id="ca94a-149">**Windows 8.1 引進**。</span><span class="sxs-lookup"><span data-stu-id="ca94a-149">**Introduced in Windows 8.1**.</span></span> <span data-ttu-id="ca94a-150">指定 ProgID 與副檔名為基礎的關聯。</span><span class="sxs-lookup"><span data-stu-id="ca94a-150">Specifies that the ProgID corresponds with a file extension based association.</span></span> <span data-ttu-id="ca94a-151">搭配使用 **ASSOCF \_ INIT \_ FIXED \_ PROGID**。</span><span class="sxs-lookup"><span data-stu-id="ca94a-151">Use together with **ASSOCF\_INIT\_FIXED\_PROGID**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ca94a-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca94a-152">Requirements</span></span>



| <span data-ttu-id="ca94a-153">需求</span><span class="sxs-lookup"><span data-stu-id="ca94a-153">Requirement</span></span> | <span data-ttu-id="ca94a-154">值</span><span class="sxs-lookup"><span data-stu-id="ca94a-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca94a-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca94a-155">Minimum supported client</span></span> | <span data-ttu-id="ca94a-156">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca94a-156">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span>               |
| <span data-ttu-id="ca94a-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca94a-157">Minimum supported server</span></span> | <span data-ttu-id="ca94a-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca94a-158">Windows 2000 Server \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="ca94a-159">標頭</span><span class="sxs-lookup"><span data-stu-id="ca94a-159">Header</span></span>                   |  <span data-ttu-id="ca94a-160">Shlwapi。h</span><span class="sxs-lookup"><span data-stu-id="ca94a-160">Shlwapi.h</span></span>  |



## <a name="see-also"></a><span data-ttu-id="ca94a-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca94a-161">See also</span></span>

 <span data-ttu-id="ca94a-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span><span class="sxs-lookup"><span data-stu-id="ca94a-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span></span> 

 

 

<span data-ttu-id="ca94a-163">© 2017 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ca94a-163">© 2017 Microsoft.</span></span> <span data-ttu-id="ca94a-164">著作權所有，並保留一切權利。</span><span class="sxs-lookup"><span data-stu-id="ca94a-164">All rights reserved.</span></span>
