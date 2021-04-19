---
description: 數值常數，指定某些 Microsoft 密碼編譯提供者在取得使用者識別碼時將使用的最大字元數。
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: 'MAXUIDLEN (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986368"
---
# <a name="maxuidlen"></a><span data-ttu-id="fa535-103">MAXUIDLEN</span><span class="sxs-lookup"><span data-stu-id="fa535-103">MAXUIDLEN</span></span>

<span data-ttu-id="fa535-104">MAXUIDLEN 是一個數值常數，可指定某些 Microsoft 密碼編譯提供者在取得使用者識別碼時將使用的最大字元數。 MAXUIDLEN 定義于 Wincrypt 中。</span><span class="sxs-lookup"><span data-stu-id="fa535-104">MAXUIDLEN is a numeric constant that specifies the maximum number of characters that some of the Microsoft cryptographic providers will use when obtaining the user ID.MAXUIDLEN is defined in Wincrypt.h.</span></span>



| <span data-ttu-id="fa535-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="fa535-105">Constant/value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="fa535-106">Description</span><span class="sxs-lookup"><span data-stu-id="fa535-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <span data-ttu-id="fa535-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="fa535-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span></span> </dl> | <span data-ttu-id="fa535-108">當 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)函式的 *PszContainer* 參數為 **Null** 時，某些 Microsoft 密碼編譯提供者會使用目前登入之使用者的登入名稱做為金鑰容器名稱。</span><span class="sxs-lookup"><span data-stu-id="fa535-108">When the *pszContainer* parameter of the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function is **NULL**, some of the Microsoft cryptographic providers use the logon name of the currently logged on user as the key container name.</span></span> <span data-ttu-id="fa535-109">MAXUIDLEN 指定這些提供者將用於使用者名稱的字元數上限，包括結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="fa535-109">MAXUIDLEN specifies the maximum number of characters, including the terminating **NULL** character, that these providers will use for the user name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fa535-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa535-110">Requirements</span></span>



| <span data-ttu-id="fa535-111">需求</span><span class="sxs-lookup"><span data-stu-id="fa535-111">Requirement</span></span> | <span data-ttu-id="fa535-112">值</span><span class="sxs-lookup"><span data-stu-id="fa535-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa535-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa535-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fa535-114">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa535-114">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fa535-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa535-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fa535-116">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa535-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa535-117">標頭</span><span class="sxs-lookup"><span data-stu-id="fa535-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa535-118"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa535-118"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa535-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa535-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa535-120">**CryptAcquireCoNtext**</span><span class="sxs-lookup"><span data-stu-id="fa535-120">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[<span data-ttu-id="fa535-121">**CPAcquireCoNtext**</span><span class="sxs-lookup"><span data-stu-id="fa535-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




