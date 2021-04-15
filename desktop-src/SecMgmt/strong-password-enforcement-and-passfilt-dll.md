---
description: 列出強式密碼系統管理工具所強制執行的需求。
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: 強式密碼強制執行和 Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511164"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a><span data-ttu-id="7e587-103">強式密碼強制執行和 Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="7e587-103">Strong Password Enforcement and Passfilt.dll</span></span>

<span data-ttu-id="7e587-104">您可以使用系統管理工具來啟用強式密碼強制。</span><span class="sxs-lookup"><span data-stu-id="7e587-104">Strong password enforcement can be enabled by using the system administration tools.</span></span> <span data-ttu-id="7e587-105">如果已啟用系統管理原則，則在建立或變更密碼時，密碼必須符合下列最低需求：</span><span class="sxs-lookup"><span data-stu-id="7e587-105">If the system administration policy is enabled, passwords must meet the following minimum requirements when they are created or changed:</span></span>

-   <span data-ttu-id="7e587-106">密碼可能不會包含使用者的 samAccountName (帳戶名稱) 值或整個 displayName (完整名稱值) 。</span><span class="sxs-lookup"><span data-stu-id="7e587-106">Passwords may not contain the user's samAccountName (Account Name) value or entire displayName (Full Name value).</span></span> <span data-ttu-id="7e587-107">這兩種檢查不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7e587-107">Both checks are not case sensitive.</span></span>
-   <span data-ttu-id="7e587-108">SamAccountName 會完整地簽入，以判斷它是否為密碼的一部分。</span><span class="sxs-lookup"><span data-stu-id="7e587-108">The samAccountName is checked in its entirety only to determine whether it is part of the password.</span></span> <span data-ttu-id="7e587-109">如果 samAccountName 長度少於三個字元，則會略過此檢查。</span><span class="sxs-lookup"><span data-stu-id="7e587-109">If the samAccountName is less than three characters long, this check is skipped.</span></span>
-   <span data-ttu-id="7e587-110">DisplayName 會針對分隔符號進行剖析：逗號、句號、連字號或連字號、底線、空格、字型大小及定位字元。</span><span class="sxs-lookup"><span data-stu-id="7e587-110">The displayName is parsed for delimiters: commas, periods, dashes or hyphens, underscores, spaces, pound signs, and tabs.</span></span> <span data-ttu-id="7e587-111">如果找到任何這些分隔符號，則會分割 displayName，並確認 (token) 的所有剖析區段都不會包含在密碼中。</span><span class="sxs-lookup"><span data-stu-id="7e587-111">If any of these delimiters are found, the displayName is split and all parsed sections (tokens) are confirmed to not be included in the password.</span></span> <span data-ttu-id="7e587-112">系統會忽略小於三個字元的權杖，而且不會檢查標記的子字串。</span><span class="sxs-lookup"><span data-stu-id="7e587-112">Tokens that are less than three characters are ignored, and substrings of the tokens are not checked.</span></span> <span data-ttu-id="7e587-113">例如，名稱 "Erin M. Hagens" 會分割成三個標記： "Erin"、"M" 和 "Hagens"。</span><span class="sxs-lookup"><span data-stu-id="7e587-113">For example, the name "Erin M. Hagens" is split into three tokens: "Erin", "M", and "Hagens".</span></span> <span data-ttu-id="7e587-114">因為第二個權杖的長度只是一個字元，所以會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7e587-114">Because the second token is only one character long, it is ignored.</span></span> <span data-ttu-id="7e587-115">因此，此使用者的密碼不能包含 "erin" 或 "hagens" 做為密碼中任何位置的子字串。</span><span class="sxs-lookup"><span data-stu-id="7e587-115">Therefore, this user could not have a password that included either "erin" or "hagens" as a substring anywhere in the password.</span></span>
-   <span data-ttu-id="7e587-116">密碼必須包含下列五個類別中的三個字元。</span><span class="sxs-lookup"><span data-stu-id="7e587-116">Passwords must contain characters from three of the five following categories.</span></span>



| <span data-ttu-id="7e587-117">字元類別</span><span class="sxs-lookup"><span data-stu-id="7e587-117">Character categories</span></span>                                                                                                                                                      | <span data-ttu-id="7e587-118">範例</span><span class="sxs-lookup"><span data-stu-id="7e587-118">Examples</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="7e587-119">歐洲語言的大寫字母 (A 至 Z，包含變音符號、希臘文和斯拉夫文字元) </span><span class="sxs-lookup"><span data-stu-id="7e587-119">Uppercase letters of European languages (A through Z, with diacritic marks, Greek and Cyrillic characters)</span></span><br/>                                                     | <span data-ttu-id="7e587-120">A、B、C、Z</span><span class="sxs-lookup"><span data-stu-id="7e587-120">A, B, C,   Z</span></span><br/>                |
| <span data-ttu-id="7e587-121">歐洲語言的小寫字母 (a 至 z、銳角、變音符號、希臘文及斯拉夫文字元) </span><span class="sxs-lookup"><span data-stu-id="7e587-121">Lowercase letters of European languages (a through z, sharp-s, with diacritic marks, Greek and Cyrillic characters)</span></span><br/>                                            | <span data-ttu-id="7e587-122">a、b、c、z</span><span class="sxs-lookup"><span data-stu-id="7e587-122">a, b, c,   z</span></span><br/>                |
| <span data-ttu-id="7e587-123">以 10 為基底的數字 (0 到 9)。</span><span class="sxs-lookup"><span data-stu-id="7e587-123">Base 10 digits (0 through 9)</span></span><br/>                                                                                                                                   | <span data-ttu-id="7e587-124">0、1、2、9</span><span class="sxs-lookup"><span data-stu-id="7e587-124">0, 1, 2,   9</span></span><br/>                |
| <span data-ttu-id="7e587-125"> (特殊字元的非英數位元) </span><span class="sxs-lookup"><span data-stu-id="7e587-125">Non-alphanumeric characters (special characters)</span></span><br/>                                                                                                               | <span data-ttu-id="7e587-126">$,!,%，^， () {} \[ \] ;： <>？</span><span class="sxs-lookup"><span data-stu-id="7e587-126">$,!,%,^,(){}\[\];:<>?</span></span><br/> |
| <span data-ttu-id="7e587-127">分類為字母字元但不是大寫或小寫的任何 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="7e587-127">Any Unicode character that is categorized as an alphabetic character but is not uppercase or lowercase.</span></span> <span data-ttu-id="7e587-128">這包括亞洲語言的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="7e587-128">This includes Unicode characters from Asian languages.</span></span><br/> |                                        |



 

<span data-ttu-id="7e587-129">**若要啟用強式密碼強制**</span><span class="sxs-lookup"><span data-stu-id="7e587-129">**To enable strong password enforcement**</span></span>

1.  <span data-ttu-id="7e587-130">從管理主控台找出 [ **本機安全性原則**]。</span><span class="sxs-lookup"><span data-stu-id="7e587-130">From the administration console, locate **Local Security Policy**.</span></span>
2.  <span data-ttu-id="7e587-131">選取 [ **帳戶原則**]，然後選取 [ **密碼原則**]。</span><span class="sxs-lookup"><span data-stu-id="7e587-131">Select **Account Policy**, and then select **Password Policy**.</span></span>
3.  <span data-ttu-id="7e587-132">[啟用 **密碼必須符合複雜性需求** ] 設定。</span><span class="sxs-lookup"><span data-stu-id="7e587-132">Enable the **Passwords must meet complexity requirements** setting.</span></span>

> [!Note]  
> <span data-ttu-id="7e587-133">指定的字元只能滿足一個類別目錄。</span><span class="sxs-lookup"><span data-stu-id="7e587-133">A given character can satisfy only one category.</span></span> <span data-ttu-id="7e587-134">[GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew)函式可用來測試密碼中的每個字元是否為大寫、小寫或英數位元。</span><span class="sxs-lookup"><span data-stu-id="7e587-134">The [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) function is used to test whether each character in the password is uppercase, lowercase, or alphanumeric.</span></span>

 

 

