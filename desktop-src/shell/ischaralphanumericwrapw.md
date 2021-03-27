---
description: 判斷字元是否為字母或數位字元。
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972433"
---
# <a name="ischaralphanumericwrapw-function"></a><span data-ttu-id="b808d-103">IsCharAlphaNumericWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="b808d-103">IsCharAlphaNumericWrapW function</span></span>

<span data-ttu-id="b808d-104">\[**IsCharAlphaNumericWrapW** 可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="b808d-104">\[**IsCharAlphaNumericWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="b808d-105">在後續版本中將無法使用。</span><span class="sxs-lookup"><span data-stu-id="b808d-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="b808d-106">您應該在其位置使用 [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 。\]</span><span class="sxs-lookup"><span data-stu-id="b808d-106">You should use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in its place.\]</span></span>

<span data-ttu-id="b808d-107">判斷字元是否為字母或數位字元。</span><span class="sxs-lookup"><span data-stu-id="b808d-107">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="b808d-108">這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。</span><span class="sxs-lookup"><span data-stu-id="b808d-108">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span>

> [!Note]  
> <span data-ttu-id="b808d-109">**IsCharAlphaNumericWrapW** 是 **IsCharAlphaNumericW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="b808d-109">**IsCharAlphaNumericWrapW** is a wrapper for the **IsCharAlphaNumericW** function.</span></span> <span data-ttu-id="b808d-110">如需進一步的使用注意事項，請參閱 [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 頁面。</span><span class="sxs-lookup"><span data-stu-id="b808d-110">See the [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b808d-111">語法</span><span class="sxs-lookup"><span data-stu-id="b808d-111">Syntax</span></span>


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a><span data-ttu-id="b808d-112">參數</span><span class="sxs-lookup"><span data-stu-id="b808d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b808d-113">*ch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b808d-113">*ch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b808d-114">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="b808d-114">Type: **WCHAR**</span></span>

<span data-ttu-id="b808d-115">要測試的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="b808d-115">The Unicode character to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b808d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b808d-116">Return value</span></span>

<span data-ttu-id="b808d-117">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="b808d-117">Type: **BOOL**</span></span>

<span data-ttu-id="b808d-118">如果字元是英數位元，則傳回值為非零。</span><span class="sxs-lookup"><span data-stu-id="b808d-118">If the character is alphanumeric, the return value is nonzero.</span></span>

<span data-ttu-id="b808d-119">如果字元不是英數位元，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="b808d-119">If the character is not alphanumeric, the return value is zero.</span></span> <span data-ttu-id="b808d-120">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="b808d-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b808d-121">備註</span><span class="sxs-lookup"><span data-stu-id="b808d-121">Remarks</span></span>

<span data-ttu-id="b808d-122">**IsCharAlphaNumericWrapW** 能讓您在 Windows XP 之前的作業系統中使用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="b808d-122">**IsCharAlphaNumericWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="b808d-123">慣用的方法是使用 [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="b808d-123">The preferred method is to use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="b808d-124">您必須使用序數28，直接從 Shlwapi.dll 呼叫 **IsCharAlphaNumericWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="b808d-124">**IsCharAlphaNumericWrapW** must be called directly from Shlwapi.dll, using ordinal 28.</span></span>

## <a name="requirements"></a><span data-ttu-id="b808d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b808d-125">Requirements</span></span>



| <span data-ttu-id="b808d-126">需求</span><span class="sxs-lookup"><span data-stu-id="b808d-126">Requirement</span></span> | <span data-ttu-id="b808d-127">值</span><span class="sxs-lookup"><span data-stu-id="b808d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b808d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b808d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b808d-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b808d-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b808d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b808d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b808d-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b808d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b808d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b808d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b808d-133"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b808d-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b808d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b808d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b808d-135">**IsCharAlphaNumeric**</span><span class="sxs-lookup"><span data-stu-id="b808d-135">**IsCharAlphaNumeric**</span></span>](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
