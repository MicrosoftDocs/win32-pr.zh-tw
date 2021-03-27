---
description: 為指定的使用者建立使用者設定檔。
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: CreateUserProfileEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974845"
---
# <a name="createuserprofileex-function"></a><span data-ttu-id="94dd2-103">CreateUserProfileEx 函式</span><span class="sxs-lookup"><span data-stu-id="94dd2-103">CreateUserProfileEx function</span></span>

<span data-ttu-id="94dd2-104">\[從 Windows Vista 起，無法使用此函式。\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-104">\[This function is not available as of Windows Vista.\]</span></span>

<span data-ttu-id="94dd2-105">為指定的使用者建立使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="94dd2-105">Creates a user profile for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="94dd2-106">語法</span><span class="sxs-lookup"><span data-stu-id="94dd2-106">Syntax</span></span>


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a><span data-ttu-id="94dd2-107">參數</span><span class="sxs-lookup"><span data-stu-id="94dd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94dd2-108">*pSid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-108">*pSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94dd2-109">類型： **PSID**</span><span class="sxs-lookup"><span data-stu-id="94dd2-109">Type: **PSID**</span></span>

<span data-ttu-id="94dd2-110">新使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="94dd2-110">The SID of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="94dd2-111">*lpUserName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-111">*lpUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94dd2-112">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="94dd2-112">Type: **LPCTSTR**</span></span>

<span data-ttu-id="94dd2-113">包含新使用者的使用者名稱之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="94dd2-113">Pointer to a buffer that contains the user name of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="94dd2-114">*lpUserHive* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-114">*lpUserHive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94dd2-115">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="94dd2-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="94dd2-116">包含要使用之登錄 [hive](../sysinfo/registry-hives.md) 的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="94dd2-116">Pointer to a buffer that contains the [registry hive](../sysinfo/registry-hives.md) to use.</span></span> <span data-ttu-id="94dd2-117">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="94dd2-117">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94dd2-118">*lpProfileDir* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-118">*lpProfileDir* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94dd2-119">類型： **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="94dd2-119">Type: **LPTSTR**</span></span>

<span data-ttu-id="94dd2-120">緩衝區的指標，此函式傳回時，會接收使用者的設定檔目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="94dd2-120">Pointer to a buffer that, when this function returns, receives the user's profile directory path.</span></span> <span data-ttu-id="94dd2-121">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="94dd2-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94dd2-122">*dwDirSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-122">*dwDirSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94dd2-123">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94dd2-123">Type: **DWORD**</span></span>

<span data-ttu-id="94dd2-124">*LpProfileDir* 在 TCHARs 中指定的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="94dd2-124">Size of the buffer specified by *lpProfileDir*, in TCHARs.</span></span>

</dd> <dt>

<span data-ttu-id="94dd2-125">*bWin9xUpg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-125">*bWin9xUpg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94dd2-126">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="94dd2-126">Type: **BOOL**</span></span>

<span data-ttu-id="94dd2-127">如果在從 Windows 9x 進行設定檔的過程中建立使用者設定檔，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="94dd2-127">**TRUE** if the user profile is being created as part of a profile migration from Windows 9x; otherwise, **FALSE**.</span></span>

<span data-ttu-id="94dd2-128">若 **為 TRUE**，則會在預設的設定檔目錄（通常是 C： \\ Documents 和 Settings \\ *UserName*）中設定使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="94dd2-128">When **TRUE**, the user profile is set up in the default profile directory—normally C:\\Documents and Settings\\*UserName*.</span></span> <span data-ttu-id="94dd2-129">如果該目錄已存在，則會使用它。</span><span class="sxs-lookup"><span data-stu-id="94dd2-129">If that directory already exists, it is used.</span></span> <span data-ttu-id="94dd2-130">如果沒有，則會建立它。</span><span class="sxs-lookup"><span data-stu-id="94dd2-130">If it does not, it is created.</span></span>

<span data-ttu-id="94dd2-131">如果 **為 FALSE**，則會建立預設的設定檔目錄（如果不存在的話）。</span><span class="sxs-lookup"><span data-stu-id="94dd2-131">If **FALSE**, the default profile directory is created if it does not exist.</span></span> <span data-ttu-id="94dd2-132">如果預設的設定檔目錄已存在，則會建立此使用者設定檔的新目錄。</span><span class="sxs-lookup"><span data-stu-id="94dd2-132">If the default profile directory already exists, a new directory is created for this user profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94dd2-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="94dd2-133">Return value</span></span>

<span data-ttu-id="94dd2-134">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="94dd2-134">Type: **BOOL**</span></span>

<span data-ttu-id="94dd2-135">如果已成功建立新的使用者設定檔，則傳回 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="94dd2-135">Returns **TRUE** if the new user profile was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="94dd2-136">備註</span><span class="sxs-lookup"><span data-stu-id="94dd2-136">Remarks</span></span>

<span data-ttu-id="94dd2-137">此函式未在軟體發展工具組中宣告 (SDK) 標頭，且沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="94dd2-137">This function is not declared in the software development kit (SDK) headers and has no associated import library.</span></span> <span data-ttu-id="94dd2-138">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數連結至 Userenv.dll。</span><span class="sxs-lookup"><span data-stu-id="94dd2-138">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to link to Userenv.dll.</span></span> <span data-ttu-id="94dd2-139">函數的 ANSI 版本， **CreateUserProfileExA** 會從 Userenv.dll 參考為序數153。</span><span class="sxs-lookup"><span data-stu-id="94dd2-139">The ANSI version of the function, **CreateUserProfileExA** is referenced from Userenv.dll as ordinal 153.</span></span> <span data-ttu-id="94dd2-140">Unicode 版本 **CreateUserProfileExW** 是以序數154的形式參考。</span><span class="sxs-lookup"><span data-stu-id="94dd2-140">The Unicode version, **CreateUserProfileExW** is referenced as ordinal 154.</span></span>

## <a name="requirements"></a><span data-ttu-id="94dd2-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="94dd2-141">Requirements</span></span>



| <span data-ttu-id="94dd2-142">需求</span><span class="sxs-lookup"><span data-stu-id="94dd2-142">Requirement</span></span> | <span data-ttu-id="94dd2-143">值</span><span class="sxs-lookup"><span data-stu-id="94dd2-143">Value</span></span> |
|-----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94dd2-144">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="94dd2-144">End of client support</span></span><br/>  | <span data-ttu-id="94dd2-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="94dd2-145">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="94dd2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="94dd2-146">DLL</span></span><br/>                    | <dl> <span data-ttu-id="94dd2-147"><dt>Userenv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94dd2-147"><dt>Userenv.dll</dt></span></span> </dl> |
| <span data-ttu-id="94dd2-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="94dd2-148">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="94dd2-149">**CreateUserProfileExW** (Unicode) 和 **CreateUserProfileExA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="94dd2-149">**CreateUserProfileExW** (Unicode) and **CreateUserProfileExA** (ANSI)</span></span><br/>      |



 

 
