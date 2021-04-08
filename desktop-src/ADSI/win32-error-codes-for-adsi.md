---
title: ADSI 的 Win32 錯誤碼
description: 標準 Win32 錯誤碼也用來傳回 ADSI 錯誤訊息。
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- ADSI 的 Win32 錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671099"
---
# <a name="win32-error-codes-for-adsi"></a><span data-ttu-id="784d5-104">ADSI 的 Win32 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="784d5-104">Win32 Error Codes for ADSI</span></span>

<span data-ttu-id="784d5-105">標準 Win32 錯誤碼也用來傳回 ADSI 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="784d5-105">Standard Win32 error codes are also used to return ADSI error messages.</span></span> <span data-ttu-id="784d5-106">具體而言，ADSI LDAP 提供者會將所有 LDAP 錯誤碼對應至 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="784d5-106">Specifically, the ADSI LDAP provider maps all the LDAP error codes to Win32 error codes.</span></span> <span data-ttu-id="784d5-107">這些錯誤碼的 **HRESULT** 值是0x8007XXXX 格式，其中最後四個十六進位數位（XXXX）對應到適當 Win32 錯誤碼的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="784d5-107">The **HRESULT** values of these error codes are of the 0x8007XXXX format, where the last four hexadecimal digits, XXXX, corresponds to the **DWORD** values of the appropriate Win32 error code.</span></span> <span data-ttu-id="784d5-108">例如，ADSI 錯誤值0x80072020 會以十進位的十六進位或8224提供0x2020 的 Win32 誤差值。</span><span class="sxs-lookup"><span data-stu-id="784d5-108">For example, the ADSI error value 0x80072020 gives the Win32 error value of 0x2020 in hexadecimal or 8224 in decimal.</span></span>

<span data-ttu-id="784d5-109">若要將您應用程式傳回的 ADSI 錯誤碼 **HRESULT** 值轉換為對應的 Win32 error **DWORD** 值（如上述標頭檔中所定義），請使用下列程式。</span><span class="sxs-lookup"><span data-stu-id="784d5-109">To convert the **HRESULT** value of an ADSI error code, returned by your application, to the corresponding the Win32 error **DWORD** value, as defined in the header files above, use the following procedure.</span></span>

<span data-ttu-id="784d5-110">ADSI 的大部分 Win32 錯誤碼都定義于 Winerror.h .h 或 Lmerr 中。</span><span class="sxs-lookup"><span data-stu-id="784d5-110">Most of the Win32 error codes for ADSI are defined in Winerror.h or Lmerr.h.</span></span> <span data-ttu-id="784d5-111">這些檔案中的錯誤值會列為十進位值。</span><span class="sxs-lookup"><span data-stu-id="784d5-111">The error values are listed as decimal values in these files.</span></span>

<span data-ttu-id="784d5-112">**將 ADSI 錯誤碼的 **HRESULT** 值轉換為對應的 Win32 error **DWORD** 值**</span><span class="sxs-lookup"><span data-stu-id="784d5-112">**To convert the **HRESULT** value of an ADSI error code to the corresponding the Win32 error **DWORD** value**</span></span>

1.  <span data-ttu-id="784d5-113">如果開頭為十進位值，則將 **HRESULT** 值轉換為十六進位數位，如同您可能從 Visual Basic 應用程式取得的值。</span><span class="sxs-lookup"><span data-stu-id="784d5-113">Convert the **HRESULT** value to a hexadecimal number if starting with a decimal value as you may get from a Visual Basic application.</span></span>
2.  <span data-ttu-id="784d5-114">捨棄0x8007 元件會產生餘數。</span><span class="sxs-lookup"><span data-stu-id="784d5-114">Drop the 0x8007 part produce the remainder.</span></span>
3.  <span data-ttu-id="784d5-115">將餘數轉換成十進位數。</span><span class="sxs-lookup"><span data-stu-id="784d5-115">Convert the remainder to a decimal number.</span></span>
4.  <span data-ttu-id="784d5-116">在 Winerror.h 中查詢小數餘數。</span><span class="sxs-lookup"><span data-stu-id="784d5-116">Look up the decimal remainder in Winerror.h.</span></span>
5.  <span data-ttu-id="784d5-117">如果在 Winerror.h 中找不到，請從小數餘數減去2100，並在 Lmerr 中查詢結果。</span><span class="sxs-lookup"><span data-stu-id="784d5-117">If not found in Winerror.h, subtract 2100 from the decimal remainder and look up the result in Lmerr.h.</span></span>

<span data-ttu-id="784d5-118">ADSI 2.0 會將 LDAP 錯誤碼對應到一組 Win32 錯誤碼，而這組程式碼與 ADSI 中用於 Windows 2000 和 DS 用戶端的錯誤碼不同。</span><span class="sxs-lookup"><span data-stu-id="784d5-118">ADSI 2.0 maps the LDAP error codes to a set of Win32 error codes that is different from that used in ADSI for Windows 2000 and DS Client.</span></span> <span data-ttu-id="784d5-119">這些差異列在：</span><span class="sxs-lookup"><span data-stu-id="784d5-119">The differences are listed in:</span></span>

-   [<span data-ttu-id="784d5-120">Win32 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="784d5-120">Win32 Error Codes</span></span>](win32-error-codes.md)
-   [<span data-ttu-id="784d5-121">ADSI 2.0 的 Win32 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="784d5-121">Win32 Error Codes for ADSI 2.0</span></span>](win32-error-codes-for-adsi-2-0.md)

 

 




