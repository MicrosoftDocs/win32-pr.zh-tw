---
description: 將地區設定識別碼轉換為地區設定名稱。
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: 'DownlevelLCIDToLocaleName 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980001"
---
# <a name="downlevellcidtolocalename-function"></a><span data-ttu-id="31856-103">DownlevelLCIDToLocaleName 函式</span><span class="sxs-lookup"><span data-stu-id="31856-103">DownlevelLCIDToLocaleName function</span></span>

<span data-ttu-id="31856-104">將 [地區設定識別碼](locale-identifiers.md) 轉換為 [地區設定名稱](locale-names.md)。</span><span class="sxs-lookup"><span data-stu-id="31856-104">Converts a [locale identifier](locale-identifiers.md) to a [locale name](locale-names.md).</span></span>

> [!Note]  
> <span data-ttu-id="31856-105">只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="31856-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="31856-106">其用途需要下載套件。</span><span class="sxs-lookup"><span data-stu-id="31856-106">Its use requires a download package.</span></span> <span data-ttu-id="31856-107">只在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) 來取得地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="31856-107">Applications that run only on Windows Vista and later should call [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to retrieve a locale name.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="31856-108">語法</span><span class="sxs-lookup"><span data-stu-id="31856-108">Syntax</span></span>


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="31856-109">參數</span><span class="sxs-lookup"><span data-stu-id="31856-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31856-110">*地區* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="31856-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31856-111">要轉譯的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="31856-111">The locale identifier to translate.</span></span> <span data-ttu-id="31856-112">您可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="31856-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier.</span></span> <span data-ttu-id="31856-113">此函式不支援中性地區設定或下列特定地區設定識別碼值。</span><span class="sxs-lookup"><span data-stu-id="31856-113">This function does not support neutral locales or the following specific locale identifier values.</span></span>

-   [<span data-ttu-id="31856-114">地區設定 \_ 系統 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="31856-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="31856-115">地區設定 \_ 使用者 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="31856-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)
-   [<span data-ttu-id="31856-116">地區設定 \_ 自訂 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="31856-116">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="31856-117">地區設定 \_ 自訂 \_ UI \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="31856-117">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="31856-118">未指定地區設定的 \_ 自訂 \_</span><span class="sxs-lookup"><span data-stu-id="31856-118">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> <dt>

<span data-ttu-id="31856-119">*lpName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="31856-119">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31856-120">緩衝區的指標，此函式會在此函數中抓取地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="31856-120">Pointer to a buffer in which this function retrieves the locale name.</span></span> <span data-ttu-id="31856-121">如果 *cchName* 設為0，則函式會抓取 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="31856-121">The function retrieves **NULL** if *cchName* is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="31856-122">*cchName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31856-122">*cchName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31856-123">地區設定名稱緩衝區的大小（以 UTF-16 編碼點）。</span><span class="sxs-lookup"><span data-stu-id="31856-123">Size, in UTF-16 code points, of the locale name buffer.</span></span> <span data-ttu-id="31856-124">應用程式會將此參數設定為0，以傳回地區設定名稱緩衝區所需的大小。</span><span class="sxs-lookup"><span data-stu-id="31856-124">The application sets this parameter to 0 to return the required size of the locale name buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31856-125">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31856-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31856-126">旗標，指定要取出的名稱類型。</span><span class="sxs-lookup"><span data-stu-id="31856-126">Flags specifying the type of name to retrieve.</span></span> <span data-ttu-id="31856-127">預設值為下層 \_ 地區設定 \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="31856-127">The default value is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31856-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="31856-128">Return value</span></span>

<span data-ttu-id="31856-129">傳回地區設定名稱中 UTF-16 程式碼點的計數，如果成功，則包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="31856-129">Returns the count of UTF-16 code points in the locale name, including the terminating null character, if successful.</span></span> <span data-ttu-id="31856-130">如果函式成功，而且 *cchName* 的值為0，則傳回值會是所需的大小（以字元為單位）， (包含 null 字元) ）作為地區設定名稱緩衝區。</span><span class="sxs-lookup"><span data-stu-id="31856-130">If the function succeeds and the value of *cchName* is 0, the return value is the required size, in characters (including null characters), for the locale name buffer.</span></span>

<span data-ttu-id="31856-131">如果不成功，函數會傳回0。</span><span class="sxs-lookup"><span data-stu-id="31856-131">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="31856-132">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="31856-132">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="31856-133">\_緩衝區不足 \_ 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="31856-133">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="31856-134">提供的緩衝區大小不夠大，或未正確設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31856-134">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="31856-135">錯誤 \_ 無效 \_ 的旗標。</span><span class="sxs-lookup"><span data-stu-id="31856-135">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="31856-136">*DwFlags* 的值無效。</span><span class="sxs-lookup"><span data-stu-id="31856-136">The value of *dwFlags* is not valid.</span></span>
-   <span data-ttu-id="31856-137">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="31856-137">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="31856-138">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="31856-138">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="31856-139">備註</span><span class="sxs-lookup"><span data-stu-id="31856-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="31856-140">此函數不支援 [自訂地區](custom-locales.md)設定。</span><span class="sxs-lookup"><span data-stu-id="31856-140">This function does not support [custom locales](custom-locales.md).</span></span>

 

<span data-ttu-id="31856-141">必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。</span><span class="sxs-lookup"><span data-stu-id="31856-141">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="31856-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="31856-142">Requirements</span></span>



| <span data-ttu-id="31856-143">需求</span><span class="sxs-lookup"><span data-stu-id="31856-143">Requirement</span></span> | <span data-ttu-id="31856-144">值</span><span class="sxs-lookup"><span data-stu-id="31856-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31856-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31856-145">Minimum supported client</span></span><br/> | <span data-ttu-id="31856-146">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31856-146">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="31856-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31856-147">Minimum supported server</span></span><br/> | <span data-ttu-id="31856-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31856-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="31856-149">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="31856-149">Redistributable</span></span><br/>          | <span data-ttu-id="31856-150">Microsoft NLS 下層資料對應 Api 于 windows XP SP2 和 laterorWindows Vista</span><span class="sxs-lookup"><span data-stu-id="31856-150">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="31856-151">標頭</span><span class="sxs-lookup"><span data-stu-id="31856-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="31856-152"><dt>Nlsdl。h</dt></span><span class="sxs-lookup"><span data-stu-id="31856-152"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="31856-153">DLL</span><span class="sxs-lookup"><span data-stu-id="31856-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31856-154"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31856-154"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="31856-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31856-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31856-156">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="31856-156">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="31856-157">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="31856-157">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="31856-158">對應地區設定資料</span><span class="sxs-lookup"><span data-stu-id="31856-158">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="31856-159">**LCIDToLocaleName**</span><span class="sxs-lookup"><span data-stu-id="31856-159">**LCIDToLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
