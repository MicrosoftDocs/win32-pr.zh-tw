---
description: 抓取所提供地區設定之父系的地區設定名稱。
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: 'DownlevelGetParentLocaleName 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945064"
---
# <a name="downlevelgetparentlocalename-function"></a><span data-ttu-id="7c2fe-103">DownlevelGetParentLocaleName 函式</span><span class="sxs-lookup"><span data-stu-id="7c2fe-103">DownlevelGetParentLocaleName function</span></span>

<span data-ttu-id="7c2fe-104">抓取所提供地區設定之父系的 [地區設定名稱](locale-names.md) 。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-104">Retrieves the [locale name](locale-names.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="7c2fe-105">只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="7c2fe-106">其用途需要下載套件。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-106">Its use requires the download package.</span></span> <span data-ttu-id="7c2fe-107">只有在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ，並將 *LCType* 設定為 [地區設定 \_ SPARENT](locale-sparent.md)。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7c2fe-108">語法</span><span class="sxs-lookup"><span data-stu-id="7c2fe-108">Syntax</span></span>


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a><span data-ttu-id="7c2fe-109">參數</span><span class="sxs-lookup"><span data-stu-id="7c2fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c2fe-110">*地區* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="7c2fe-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2fe-111">地區設定的[地區設定識別碼](locale-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-111">[Locale identifier](locale-identifiers.md) of the locale.</span></span> <span data-ttu-id="7c2fe-112">您可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼，或使用下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="7c2fe-113">地區設定不 \_ 變</span><span class="sxs-lookup"><span data-stu-id="7c2fe-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="7c2fe-114">地區設定 \_ 系統 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="7c2fe-115">地區設定 \_ 使用者 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="7c2fe-116">**Windows Vista 和更新版本：** 也支援下列自訂地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="7c2fe-117">地區設定 \_ 自訂 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="7c2fe-118">地區設定 \_ 自訂 \_ UI \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="7c2fe-119">未指定地區設定的 \_ 自訂 \_</span><span class="sxs-lookup"><span data-stu-id="7c2fe-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="7c2fe-120">*lpName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7c2fe-120">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2fe-121">緩衝區的指標，函式會在其中抓取父地區設定名稱，或下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-121">Pointer to a buffer in which the function retrieves the parent locale name, or one of the following predefined values.</span></span> <span data-ttu-id="7c2fe-122">如果 *cchName* 設為0，則這個參數會設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-122">This parameter is set to **NULL** if *cchName* is set to 0.</span></span>

-   [<span data-ttu-id="7c2fe-123">地區設定 \_ 名稱不 \_ 變</span><span class="sxs-lookup"><span data-stu-id="7c2fe-123">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="7c2fe-124">地區設定 \_ 名稱 \_ 系統 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-124">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="7c2fe-125">地區設定 \_ 名稱 \_ 使用者 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-125">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="7c2fe-126">*cchName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c2fe-126">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2fe-127">*LpName* 在 utf-16 程式碼點中指出的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-127">Size of the buffer indicated by *lpName*, in UTF-16 code points.</span></span> <span data-ttu-id="7c2fe-128">這個參數的值為0時，會導致函式忽略 *lpName* 緩衝區，並傳回緩衝區的大小（以包含父地區設定名稱的字元 (null 字元) ）。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-128">A value of 0 for this parameter causes the function to ignore the *lpName* buffer and return the size of the buffer, in characters (null characters included), required to contain the parent locale name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c2fe-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-129">Return value</span></span>

<span data-ttu-id="7c2fe-130">傳回地區設定名稱中 UTF-16 程式碼點的計數，如果成功，則包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-130">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span>

<span data-ttu-id="7c2fe-131">如果不成功，則此函式會傳回0。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-131">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="7c2fe-132">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="7c2fe-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="7c2fe-133">\_緩衝區不足 \_ 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="7c2fe-134">提供的緩衝區大小不夠大，或未正確設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="7c2fe-135">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-135">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="7c2fe-136">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-136">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c2fe-137">備註</span><span class="sxs-lookup"><span data-stu-id="7c2fe-137">Remarks</span></span>

<span data-ttu-id="7c2fe-138">必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。</span><span class="sxs-lookup"><span data-stu-id="7c2fe-138">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c2fe-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c2fe-139">Requirements</span></span>



| <span data-ttu-id="7c2fe-140">需求</span><span class="sxs-lookup"><span data-stu-id="7c2fe-140">Requirement</span></span> | <span data-ttu-id="7c2fe-141">值</span><span class="sxs-lookup"><span data-stu-id="7c2fe-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2fe-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c2fe-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7c2fe-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c2fe-143">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c2fe-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c2fe-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7c2fe-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c2fe-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c2fe-146">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7c2fe-146">Redistributable</span></span><br/>          | <span data-ttu-id="7c2fe-147">Microsoft NLS 下層資料對應 Api 于 windows XP SP2 和更新版本</span><span class="sxs-lookup"><span data-stu-id="7c2fe-147">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and later</span></span><br/>  |
| <span data-ttu-id="7c2fe-148">標頭</span><span class="sxs-lookup"><span data-stu-id="7c2fe-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c2fe-149"><dt>Nlsdl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2fe-149"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="7c2fe-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7c2fe-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c2fe-151"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c2fe-151"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c2fe-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c2fe-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2fe-153">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="7c2fe-153">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="7c2fe-154">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="7c2fe-154">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="7c2fe-155">對應地區設定資料</span><span class="sxs-lookup"><span data-stu-id="7c2fe-155">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="7c2fe-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="7c2fe-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
