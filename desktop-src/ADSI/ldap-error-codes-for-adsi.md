---
title: ADSI 的 LDAP 錯誤碼
description: 當 LDAP 伺服器產生錯誤並將錯誤傳遞給用戶端時，LDAP 用戶端就會將錯誤轉譯成字串。
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839168"
---
# <a name="ldap-error-codes-for-adsi"></a><span data-ttu-id="a8adf-103">ADSI 的 LDAP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a8adf-103">LDAP Error Codes for ADSI</span></span>

<span data-ttu-id="a8adf-104">當 LDAP 伺服器產生錯誤並將錯誤傳遞給用戶端時，LDAP 用戶端就會將錯誤轉譯成字串。</span><span class="sxs-lookup"><span data-stu-id="a8adf-104">When an LDAP server generates an error and passes the error to the client, the error is then translated into a string by the LDAP client.</span></span>

<span data-ttu-id="a8adf-105">這個方法類似于 [ADSI 的 Win32 錯誤碼](win32-error-codes-for-adsi.md)。</span><span class="sxs-lookup"><span data-stu-id="a8adf-105">This method is similar to [Win32 error codes for ADSI](win32-error-codes-for-adsi.md).</span></span> <span data-ttu-id="a8adf-106">在此範例中，用戶端錯誤碼是 WIN32 error 0x80072020。</span><span class="sxs-lookup"><span data-stu-id="a8adf-106">In this example, the client error code is the WIN32 error 0x80072020.</span></span>

<span data-ttu-id="a8adf-107">**判斷 ADSI 的 LDAP 錯誤碼**</span><span class="sxs-lookup"><span data-stu-id="a8adf-107">**To Determine the LDAP error codes for ADSI**</span></span>

1.  <span data-ttu-id="a8adf-108">從 WIN32 錯誤碼卸載8007。</span><span class="sxs-lookup"><span data-stu-id="a8adf-108">Drop the 8007 from the WIN32 error code.</span></span> <span data-ttu-id="a8adf-109">在此範例中，其餘的十六進位值為2020。</span><span class="sxs-lookup"><span data-stu-id="a8adf-109">In the example, the remaining hex value is 2020.</span></span>
2.  <span data-ttu-id="a8adf-110">將其餘的十六進位值轉換成十進位值。</span><span class="sxs-lookup"><span data-stu-id="a8adf-110">Convert the remaining hex value to a decimal value.</span></span> <span data-ttu-id="a8adf-111">在此範例中，其餘的十六進位值2020會轉換成十進位值8224。</span><span class="sxs-lookup"><span data-stu-id="a8adf-111">In the example, the remaining hex value 2020 converts to the decimal value 8224.</span></span>
3.  <span data-ttu-id="a8adf-112">在 Winerror.h .h 檔案中搜尋 decimal 值的定義。</span><span class="sxs-lookup"><span data-stu-id="a8adf-112">Search in the WinError.h file for the definition of the decimal value.</span></span> <span data-ttu-id="a8adf-113">在此範例中，8224L 對應至 error **error \_ DS \_ 作業 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="a8adf-113">In the example, 8224L corresponds to the error **ERROR\_DS\_OPERATIONS\_ERROR**.</span></span>
4.  <span data-ttu-id="a8adf-114">將首碼 **錯誤 \_ DS** 取代為 **LDAP \_**。</span><span class="sxs-lookup"><span data-stu-id="a8adf-114">Replace the prefix **ERROR\_DS** with **LDAP\_**.</span></span> <span data-ttu-id="a8adf-115">在此範例中，新的定義是 **LDAP \_ 作業 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="a8adf-115">In the example, the new definition is **LDAP\_OPERATIONS\_ERROR**.</span></span>
5.  <span data-ttu-id="a8adf-116">在 Winldap .h 檔案中搜尋 LDAP 錯誤定義的值。</span><span class="sxs-lookup"><span data-stu-id="a8adf-116">Search in the Winldap.h file for the value of the LDAP error definition.</span></span> <span data-ttu-id="a8adf-117">在此範例中，Winldap 檔中的 **LDAP \_ 作業 \_ 錯誤** 值為0x01。</span><span class="sxs-lookup"><span data-stu-id="a8adf-117">In the example, the value of **LDAP\_OPERATIONS\_ERROR** in the Winldap.h file is 0x01.</span></span>

 

 




