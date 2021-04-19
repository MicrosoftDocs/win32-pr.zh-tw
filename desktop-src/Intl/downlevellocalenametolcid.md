---
description: 將地區設定名稱轉換成可以用來從作業系統取得資訊的地區設定識別碼。
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: 'DownlevelLocaleNameToLCID 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980633"
---
# <a name="downlevellocalenametolcid-function"></a><span data-ttu-id="4f686-103">DownlevelLocaleNameToLCID 函式</span><span class="sxs-lookup"><span data-stu-id="4f686-103">DownlevelLocaleNameToLCID function</span></span>

<span data-ttu-id="4f686-104">將 [地區設定名稱](locale-names.md) 轉換成可以用來從作業系統取得資訊的 [地區設定識別碼](locale-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="4f686-104">Converts a [locale name](locale-names.md) to a [locale identifier](locale-identifiers.md) that can be used to get information from the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="4f686-105">只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="4f686-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="4f686-106">其用途需要下載套件。</span><span class="sxs-lookup"><span data-stu-id="4f686-106">Its use requires a download package.</span></span> <span data-ttu-id="4f686-107">只在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 來取出地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f686-107">Applications that only run on Windows Vista and later should call [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) to retrieve a locale identifier.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4f686-108">語法</span><span class="sxs-lookup"><span data-stu-id="4f686-108">Syntax</span></span>


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4f686-109">參數</span><span class="sxs-lookup"><span data-stu-id="4f686-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f686-110">*lpName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4f686-110">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f686-111">表示 [地區設定名稱](locale-names.md)之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="4f686-111">Pointer to a null-terminated string representing a [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f686-112">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4f686-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f686-113">指定名稱類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="4f686-113">Flags specifying the type of name.</span></span> <span data-ttu-id="4f686-114">預設值為下層 \_ 地區設定 \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="4f686-114">The default is DOWNLEVEL\_LOCALE\_NAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f686-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f686-115">Return value</span></span>

<span data-ttu-id="4f686-116">如果成功，則傳回對應至地區設定名稱的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f686-116">Returns the locale identifier that corresponds to the locale name if successful.</span></span>

<span data-ttu-id="4f686-117">如果不成功，函數會傳回0。</span><span class="sxs-lookup"><span data-stu-id="4f686-117">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="4f686-118">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="4f686-118">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4f686-119">錯誤 \_ 無效 \_ 的旗標。</span><span class="sxs-lookup"><span data-stu-id="4f686-119">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="4f686-120">為旗標提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="4f686-120">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="4f686-121">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="4f686-121">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4f686-122">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="4f686-122">Any of the parameter values were invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f686-123">備註</span><span class="sxs-lookup"><span data-stu-id="4f686-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f686-124">此函數不支援中性地區設定。</span><span class="sxs-lookup"><span data-stu-id="4f686-124">This function does not support neutral locales.</span></span> <span data-ttu-id="4f686-125">對等的 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 函式支援 [自訂地區](custom-locales.md)設定，但僅適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="4f686-125">The equivalent [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function supports [custom locales](custom-locales.md), but only for Windows Vista and later.</span></span>

 

<span data-ttu-id="4f686-126">必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。</span><span class="sxs-lookup"><span data-stu-id="4f686-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f686-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f686-127">Requirements</span></span>



| <span data-ttu-id="4f686-128">需求</span><span class="sxs-lookup"><span data-stu-id="4f686-128">Requirement</span></span> | <span data-ttu-id="4f686-129">值</span><span class="sxs-lookup"><span data-stu-id="4f686-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f686-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f686-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4f686-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f686-131">Windows XP \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="4f686-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f686-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4f686-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f686-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f686-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4f686-134">Redistributable</span></span><br/>          | <span data-ttu-id="4f686-135">Microsoft NLS 下層資料對應 Api 于 windows XP SP2 和 laterorWindows Vista</span><span class="sxs-lookup"><span data-stu-id="4f686-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista</span></span><br/> |
| <span data-ttu-id="4f686-136">標頭</span><span class="sxs-lookup"><span data-stu-id="4f686-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f686-137"><dt>Nlsdl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f686-137"><dt>Nlsdl.h</dt></span></span> </dl>                  |
| <span data-ttu-id="4f686-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4f686-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f686-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f686-139"><dt>NlsMap.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4f686-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f686-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f686-141">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="4f686-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4f686-142">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="4f686-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4f686-143">對應地區設定資料</span><span class="sxs-lookup"><span data-stu-id="4f686-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="4f686-144">**LocaleNameToLCID**</span><span class="sxs-lookup"><span data-stu-id="4f686-144">**LocaleNameToLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
