---
description: 抓取所提供地區設定之父系的地區設定識別碼。
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: 'DownlevelGetParentLocaleLCID 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320235"
---
# <a name="downlevelgetparentlocalelcid-function"></a><span data-ttu-id="54f36-103">DownlevelGetParentLocaleLCID 函式</span><span class="sxs-lookup"><span data-stu-id="54f36-103">DownlevelGetParentLocaleLCID function</span></span>

<span data-ttu-id="54f36-104">抓取所提供地區設定之父系的 [地區設定識別碼](locale-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="54f36-104">Retrieves the [locale identifier](locale-identifiers.md) for the parent of the supplied locale.</span></span>

> [!Note]  
> <span data-ttu-id="54f36-105">只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="54f36-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="54f36-106">其用途需要下載套件。</span><span class="sxs-lookup"><span data-stu-id="54f36-106">Its use requires the download package.</span></span> <span data-ttu-id="54f36-107">只有在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ，並將 *LCType* 設定為 [地區設定 \_ SPARENT](locale-sparent.md)。</span><span class="sxs-lookup"><span data-stu-id="54f36-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SPARENT](locale-sparent.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="54f36-108">語法</span><span class="sxs-lookup"><span data-stu-id="54f36-108">Syntax</span></span>


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a><span data-ttu-id="54f36-109">參數</span><span class="sxs-lookup"><span data-stu-id="54f36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54f36-110">*地區* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="54f36-110">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54f36-111">要取得其父地區設定識別碼之地區設定的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="54f36-111">Locale identifier of the locale for which to retrieve the parent locale identifier.</span></span> <span data-ttu-id="54f36-112">您可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼，或使用下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="54f36-112">You can use the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro to create a locale identifier or use one of the following predefined values.</span></span>

-   [<span data-ttu-id="54f36-113">地區設定不 \_ 變</span><span class="sxs-lookup"><span data-stu-id="54f36-113">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="54f36-114">地區設定 \_ 系統 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="54f36-114">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="54f36-115">地區設定 \_ 使用者 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="54f36-115">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

<span data-ttu-id="54f36-116">**Windows Vista 和更新版本：** 也支援下列自訂地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="54f36-116">**Windows Vista and later:** The following custom locale identifiers are also supported.</span></span>

-   [<span data-ttu-id="54f36-117">地區設定 \_ 自訂 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="54f36-117">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="54f36-118">地區設定 \_ 自訂 \_ UI \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="54f36-118">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="54f36-119">未指定地區設定的 \_ 自訂 \_</span><span class="sxs-lookup"><span data-stu-id="54f36-119">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54f36-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="54f36-120">Return value</span></span>

<span data-ttu-id="54f36-121">如果成功，則傳回父地區設定識別碼，否則為0。</span><span class="sxs-lookup"><span data-stu-id="54f36-121">Returns the parent locale identifier if successful, or 0 otherwise.</span></span> <span data-ttu-id="54f36-122">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="54f36-122">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="54f36-123">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="54f36-123">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="54f36-124">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="54f36-124">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="54f36-125">備註</span><span class="sxs-lookup"><span data-stu-id="54f36-125">Remarks</span></span>

<span data-ttu-id="54f36-126">必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。</span><span class="sxs-lookup"><span data-stu-id="54f36-126">The required header file and DLL are part of the "Microsoft NLS Downlevel Data Mapping APIs" download, available at the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).</span></span>

## <a name="requirements"></a><span data-ttu-id="54f36-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="54f36-127">Requirements</span></span>



| <span data-ttu-id="54f36-128">需求</span><span class="sxs-lookup"><span data-stu-id="54f36-128">Requirement</span></span> | <span data-ttu-id="54f36-129">值</span><span class="sxs-lookup"><span data-stu-id="54f36-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54f36-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54f36-130">Minimum supported client</span></span><br/> | <span data-ttu-id="54f36-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54f36-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54f36-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54f36-132">Minimum supported server</span></span><br/> | <span data-ttu-id="54f36-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54f36-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54f36-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="54f36-134">Redistributable</span></span><br/>          | <span data-ttu-id="54f36-135">Microsoft NLS 下層資料對應 Api 于 windows XPor Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54f36-135">Microsoft NLS Downlevel Data Mapping APIs onWindows XPor Windows Vista</span></span><br/>     |
| <span data-ttu-id="54f36-136">標頭</span><span class="sxs-lookup"><span data-stu-id="54f36-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="54f36-137"><dt>Nlsdl。h</dt></span><span class="sxs-lookup"><span data-stu-id="54f36-137"><dt>Nlsdl.h</dt></span></span> </dl>    |
| <span data-ttu-id="54f36-138">DLL</span><span class="sxs-lookup"><span data-stu-id="54f36-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54f36-139"><dt>NlsMap.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54f36-139"><dt>NlsMap.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54f36-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54f36-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f36-141">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="54f36-141">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="54f36-142">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="54f36-142">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="54f36-143">對應地區設定資料</span><span class="sxs-lookup"><span data-stu-id="54f36-143">Mapping Locale Data</span></span>](mapping-locale-data.md)
</dt> <dt>

[<span data-ttu-id="54f36-144">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="54f36-144">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
